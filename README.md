# Touchscreen  
[The 3.5' 320x480 resistive touchscreen made by Velleman - VMP400  ](https://www.velleman.eu/products/view/?id=438240)  
Perfect for Raspberry Pi!  

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
0   - Screen rotation 0 degrees  
90  - Screen rotation 90 degrees  
180 - Screen rotation 180 degrees  
270 - Screen rotation 270 degrees  
360 - Screen flip horizontal (Valid only for HDMI screens)  
450 - Screen flip vertical (Valid only for HDMI screens)  
```  
sudo ./rotate.sh [0] [90] [180] [270] [360] [450]  
```  

## Enable Right Click  
Add this to the `Input Class` section of either `/etc/X11/xorg.conf` or `/etc/X11/xorg.conf.d/99-calibration.conf`, depending on which exists on your Pi.  
Note that this only works when touching the touchscreen and does not change the behavior of your mouse!  
```  
   # Right mouse button is long press with pen:  
   Option "EmulateThirdButton" "1"  
   Option "EmulateThirdButtonTimeout" "750"  
   Option "EmulateThirdButtonMoveThreshold" "30"  
```  
A right click is registered by a long press. You can customize the second two parameters if you feel it is to dicciult to register a right click.  
