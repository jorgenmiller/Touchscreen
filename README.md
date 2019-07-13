# Touchscreen  
The 3.5' 320x480 resistive touchscreen made by Velleman - VMP400  

## Installation  
```  
git clone https://github.com/goodtft/LCD-show.git  
chmod -R 755 LCD-show  
cd LCD-show/  
```  

## Use Touchscreen  
This command is specific to the type of touchscreen you have. This is for the VMP400:
```  
sudo ./LCD35-show  
```  

## Use HDMI  
It is good to know how to return to use of the HDMI.
```  
sudo ./LCD-hdmi  
```  

## Rotate Display  
0-Screen rotation 0 degrees  
90-Screen rotation 90 degrees  
180-Screen rotation 180 degrees  
270-Screen rotation 270 degrees  
360-Screen flip horizontal(Valid only for HDMI screens)  
450-Screen flip vertical(Valid only for HDMI screens)  
```  
sudo ./rotate.sh [0] [90] [180] [270] [360] [450]  
```  

## To Enable Long Press for Right Click  
Add this to the `Input Class` section of either `/etc/X11/xorg.conf` or `/etc/X11/xorg.conf.d/99-calibration.conf`, depending on which exists on your Pi.  
```  
   # Right mouse button is long press with pen:  
   Option "EmulateThirdButton" "1"  
   Option "EmulateThirdButtonTimeout" "750"  
   Option "EmulateThirdButtonMoveThreshold" "30"  
```  
