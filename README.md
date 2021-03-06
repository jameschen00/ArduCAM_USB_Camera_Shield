# Overview
ArduCAM USB Camera Shield is a general purpose USB camera controller board that can accommodate wide range of CMOS camera module from 0.3MP ~ 14MP.
By using provided SDK library and demo source code, user can design their own applications.
More info can be found from [arducam website](http://www.arducam.com/arducam-usb-camera-shield-released/)

## Now Supported Cameras
-	OV7670		0.3MP
-	OV7675		0.3MP
-	OV7725		0.3MP
-	MT9V034		0.36MP (global shutter)
-	MT9M112		1.3MP	
-	MT9M001		1.3MP 	
-	AR0134		1.2MP (global shutter)
-	OV2640		2MP	
-	OV5642		5MP	
-	OV5640		5MP 
-	MT9N001		9MP
-	MT9J001		10MP
-	MT9F002		14MP

## Support OS 
- Windows
- Linux Ubuntu
- Raspbian

## Limitations
This USB camera shield has no onboard frame buffer. The transfer reliability highly depends the USB bandwidth.  
If multiple USB devices are connected to a single USB root hub, it will cause bandwidth racing and cause drop frames.  
It is recommended to preserved enough bandwidth for the camera on USB port, or reduce the frame rate and Pixel clock of the image sensor once continuously dropping frames happens.  
This USB camera shield isn't UVC compliant, for Windows you have to install our USB driver, for Linux you can use libusb which is also plug-and-play.

### PC
Basically the PC is fast enough to run ArduCAM USB camera shield without dropping frames.  
If you want to connect more than one ArduCAM USB camera shield to a single PC, you have to connect them seperately to the different USB root hub of the PC.

### Raspberry Pi
Raspberry Pi is far less processing power than PC, it is not fast enough to display the captured video by the ARM processor.  
And there is only one USB root hub on Raspberry Pi board, everything shares the USB bandwidth like the onboard ethernet and 4 USB ports.  
Running ArduCAM USB camera shield on Raspberry Pi might not as good as PC, It is recommended to do image processing without display the captured video in real time.  




