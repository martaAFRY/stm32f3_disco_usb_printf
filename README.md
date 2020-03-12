# stm32f3_disco_usb_printf

This git contains a STM32CubeIDE project for the STM32F3-discovery that uses the USB CDC class to setup a virtual terminal and implements the printf c function to print to the terminal.

This has been tested OK on Ubuntu 19.10. The STM32CubeIDE Version: 1.2.0 was used to build and flash.

Instructions

Open the project with STM32CubeIDE, File -> Open Projects from File System ...
Find the folder to where you cloned this git. Mark the stm32f3_discovery_usb_printf folder and hit "Open" and then "Finish".

You should now have the stm32f3_disco_usb_printf project setup in STM32CubeIDE. Since the launch configuration for STM32CubeIDE projects contains absolute file paths, it is not included in this git. To edit your launch configurations, open "Edit lauch configuration properties" by:
Run -> Debug As -> STM32 Cortex-M C/C++ Application
and hit "OK". After you have managed to launch like this the first time, you can just hit F11 to launch as usual afterwards.

Now, out of some reason that I haven't bothered to dig into, I need to disconnect and reconnect the "USB USER" cabel after I have Resumed/RESET the STM32F3 board otherwise the /dev/ttyASM* is buzy. Actually this is quite good since you may not know which device you'll get. So disconnect the "USER USB" cable, ls /dev/ttyASM*, then launch the project and hit F8 (Resume) if you have the first break point enabled. Then connect the "USER USB" and ls /dev/ttyASM* again. If all is well you'll see a new /dev/ttyASMn device and you can start you favorite terminal program to get the prints of your STM32F3-doscovery board.  
