SUNIX Inc. Multi-I/O Controller Windows(R) Driver.

******************************************************************************
This driver is built for the Microsoft(R) Windows Operating Systems.

Copyright 2015 SUNIX, Inc. All names mentioned herein are a registered trademark
 or a trademark of SUNIX or its respective owners. All rights reserved.
******************************************************************************

Driver Version : 8.2.0.0

Release Data : 2015/12/08


******************************************************************************
Support platform:

  Microsoft Windows 8.1 32bit/64bit
  Microsoft Windows 8   32bit/64bit
  Microsoft Windows 7 SP1 32bit/64bit
  Microsoft Windows Vista SP2 32bit/64bit

  Microsoft Windows Server 2012 R2 64bit
  Microsoft Windows Server 2012 64bit
  Microsoft Windows Server 2008 R2 SP1 64bit
  Microsoft Windows Server 2008 SP2 32bit/64bit
 
  Microsoft Windows Embedded POSReady 7 32bit/64bit
  Microsoft Windows Embedded Standard 7 SP1 32bit/64bit


******************************************************************************
DRIVER FILES:

  Setup.exe  : SUNIX Multi-I/O Controller driver package file
  readme.txt : readme text file

******************************************************************************
INSTALLATION AND REMOVAL INSTRUCTIONS:

------------------------------------------------------------------------------
Setup driver at first time (using Setup.exe)
------------------------------------------------------------------------------

NOTE :  In Windows XP/Windows Server 2003, press [Cancel] button
         if "Found New Hardware Wizard" dialog appears.

Step 1. Run Setup.exe, click [Next/Install] to continue the procedure.

Step 2. Press [Finish] to complete the installation.


------------------------------------------------------------------------------
Update driver (using Setup.exe)
------------------------------------------------------------------------------

Step 1. Run Setup.exe, click [Next/Install] to continue the procedure.

Step 2. Press [Finish] to complete the installation.


------------------------------------------------------------------------------
Remove driver (using Setup.exe)
------------------------------------------------------------------------------

Step 1. Open Programs and Features (or Add/Remove Programs),
         select "SUNIX Multi-IO Controller", and double click it to uninstall.

Step 2. Click on [Yes] to continue the procedure.

Step 3. Press [Finish] complete the uninstallation.

Step 4. Shutdown the system and remove hardware device to fully remove driver.


------------------------------------------------------------------------------
Silent installation
------------------------------------------------------------------------------

Run "Setup.exe /s /f2<path\logfile name>"
i.e. Setup.exe /s /f2c:\logfiledir\logfile.log


------------------------------------------------------------------------------
Silent uninstallation
------------------------------------------------------------------------------

Run "Setup.exe /s /uninst /f2<path\logfile name>"
i.e. Setup.exe /s /uninst /f2c:\logfiledir\logfile.log


------------------------------------------------------------------------------
Setup driver at first time (using INF file)
------------------------------------------------------------------------------

NOTE :  In Windows XP/Windows Server 2003, press [Cancel] button
         if "Found New Hardware Wizard" dialog appears.

Step 1. Open Device Manager, double click yellow marked PCI Device, PCI Serial Port, 
         PCI Parallel Port, or PCI Multiport Serial Controller to open device
         properties dialog.

Step 2. Click [Update Driver...] to install driver.

Step 3. Select "Browse my computer for driver software".

Step 4. Set driver location and press [Next].

Step 5. Close update driver dialog and device properties dialog.

Step 6. Double click yellow marked SUNIX COM Port 1 or SUNIX LPT Port 1
         to open device properties dialog, repeat step 2 to step 5 to install driver.


------------------------------------------------------------------------------
Update driver (using INF file)
------------------------------------------------------------------------------

Step 1. Open Device Manager, right click SUNIX Serial Card, SUNIX Parallel Card, 
         SUNIX Multi-I/O Card, and select [Update Driver Software...].

Step 2. Select "Browse my computer for driver software".

Step 3. Set driver location and press [Next].

Step 4. Close update driver dialog.

Step 5. Right click SUNIX COM Port 1 or SUNIX LPT Port 1, select
         [Update Driver Software...], and repeat step 2 to step 4 to update driver.


------------------------------------------------------------------------------
Remove driver (using INF file)
------------------------------------------------------------------------------

WARNING : NEVER USING THIS METHOD IF YOU HAVE USE SETUP.EXE TO INSTALL DRIVER!
           IT WILL MAKE DRIVER UNINSTALLING UNCLEANLY AND MAKE SYSTEM FAIL!

WARNING : THIS METHOD CANNOT FULLY REMOVE DRIVER FILES IN WINDOWS XP,
           WINDOWS SERVER 2003, AND WINDOWS 2000.
          DRIVER FILES ARE STILL IN THE SPECIFIC LOCATIONS.

Step 1. Open device manager.

Step 2. select SUNIX COM Port or SUNIX LPT Port, and delete it.

Step 3. Press [OK] in Confirm Device Uninstall dialog to delete device,
         and check "Delete the driver software for this device" if chechbox exists.

Step 4. Repeat step 2 to step 3 to delete all SUNIX COM Ports and SUNIX LPT Ports.

Step 5. Select SUNIX Serial Card, SUNIX Parallel Card, or SUNIX Multi-I/O Card,
         delete it, and press [OK]. If "Delete the driver software for this device"
         checkbox exists, check it before delete this device.

Step 6. Delete all SUNIX Ports and SUNIX Cards.

Step 7. Shutdown the system and remove hardware device to fully remove driver.


******************************************************************************
RELEASE NOTE:

Ver 8.2.0.0 - 2015/12/08
    0)  release version
    1)  modify driver to support specific platform
    2)  modify control sheet UI

Ver 8.1.5.0 - 2014/11/24
    0)  release version
    1)  fix a power management issue in specific platform

Ver 8.1.4.0 - 2014/06/12
    0)  release version
    1)  add ASPM selection
    2)  add 10S1P item

Ver 8.1.3.0 - 2014/01/24
    0)  release version
    1)  modify driver to support customer's request

Ver 8.1.2.0 - 2013/10/14
    0)  release version
    1)  modify SUN2000 parallel default mode function
    2)  modify driver to support customer's request

Ver 8.1.1.0 - 2013/09/13
    0)  release version
    1)  fix FIFO error issue for SUN2000 series
    2)  fix multiple parallel board issue for SUN2000 series
    3)  fix control sheet issue
    4)  fix a RS-422/485 issue
    5)  support Microsoft Windows 8.1 and Microsoft Windows Server 2012 R2

Ver 8.1.0.0 - 2013/03/28
    0)  release version
    1)  remove support for Windows 2000
    2)  modify port Hardware ID
    3)  modify property control sheet user interface
    4)  fix PLL function calculate error issue
    5)  fix parallel issue for SUN2000 series

Ver 8.0.0.0 - 2012/09/07
    0)  release version
    1)  support SUNIX SUN2000 products
    2)  support more languages
    3)  add PLL function
    4)  add parallel port default mode selection function
    5)  add enable legacy pnp detection setting in advanced control page
    6)  fix the printer icon lost issue in Windows 7
    7)  fix the driver crash issue when update driver
    8)  fix an issue sometimes COM port cannot access after driver installation

Ver 7.2.0.0 - 2010/12/07
    0)  release version
    1)  support internal/external GPIO
    2)  support 3-in-1 (RS-232/422/485) series
    3)  support more than three parallel ports
    4)  support SUNIX cash drawer kicker interface card
    5)  support SUNIX serial library
    6)  support multi-language UI
    7)  support silent installation
    8)  modify layout of control page
    9)  use driver dll to replace system default dll
   10)  fix an issue about H/W flow control setting in RS-422/485
   11)  fix an issue about the delay time of closing port
   12)  fix an issue about driver crash during change power state
   13)  fix an issue about buffer overflow

Ver 7.1.0.0 - 2010/01/13
    0)  release version
    1)  solve an issue about re-map series
    2)  support SUN1999 cardbus series
    3)  modify layout of control page
    4)  add reference clock setting in control page
    5)  add specific IoControl command to return part number

Ver 7.0.0.0 - 2009/07/14
    0)  release version
    1)  support Golden series, Matrix series, and SUN1999 series
