SUNIX Inc. Multi-I/O Controller Windows(R) Driver.

******************************************************************************
This driver is built for the Microsoft(R) Windows Operating Systems.

Copyright 2021 SUNIX, Inc. All names mentioned herein are a registered trademark
 or a trademark of SUNIX or its respective owners. All rights reserved.
******************************************************************************


Driver Version : 10.2.1.0

Release Data : 2023/03/20


******************************************************************************
Support platform:

  Microsoft Windows 11 build 22H2 64bit 
  Microsoft Windows 11 build 21H2 64bit  
  Microsoft Windows 10 build 22H2 32bit/64bit 
  Microsoft Windows 10 build 21H2 32bit/64bit  
  Microsoft Windows 10 build 21H1 32bit/64bit
  Microsoft Windows 10 build 20H2 32bit/64bit
  Microsoft Windows 10 build 2004 (20H1) 32bit/64bit 
  Microsoft Windows Server 2022 64bit 

******************************************************************************
INSTALLATION AND REMOVAL INSTRUCTIONS:

------------------------------------------------------------------------------
Setup driver at first time (using Setup.exe)
------------------------------------------------------------------------------

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

Step 1. Open Programs and Features, select "SUNIX Multi-IO Controller",
         and double click it to uninstall.

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


******************************************************************************
RELEASE NOTE:

Ver 10.2.1.0 - 2023/03/20
    0)  release version
    1)  add signing package files (dll, exe) in InstallShield release process
    2)	change some description in early driver release

Ver 10.2.1.0 - 2023/01/16
    0)  release version
    1)  fix InstallShield update process for reboot issue
    2)	remove readme-full.txt
    3)	remove DRIVER FILES section in this file

Ver 10.2.1.0 - 2022/12/26
    0)  release version
    1)	fix error reporting when old driver update to V10.1.0.0 because of SUNIX_PDO_INTERFACE structure size different

Ver 10.1.1.0 - 2022/10/04
    0)  release version
    1)  support Windows Server 2022

Ver 10.1.1.0 - 2022/09/21
    0)  release version
    1)  fix COM port can’t work resume from modern standby when opended (pofx power IRP handle, COM port resume process)

Ver 10.1.0.0_v1 - 2022/08/24
    0)  release version
    1)  recreate new driver submission

Ver 10.1.0.0 - 2022/06/30
    0)  release version
    1)  support Windows 11 build 22H2 
    2)  support Windows Server 2022

Ver 10.1.0.0 - 2021/10/15
    0)  release version
    1)  fix issue for SDV 
    2)  fix issue for CodeQL

Ver 10.0.2.0 - 2021/10/04
    0)  release version
    1)  add property page LPT polling cycle function
    2)  add property page Modern Standby always active function

Ver 10.0.1.0 - 2021/06/12
    0)  release version
    1)  fix a BSOD problem during driver updating

Ver 10.0.0.0 - 2021/06/02
    0)  release version
    1)  support 21H1 to 19H1 platforms
    2)  support DFx feature
    3)  support Modern Standby feature

Ver 9.2.2.0 - 2020/12/28
    0)  release version
    1)  support 20H2 to RS1 platforms

Ver 9.2.1.0 - 2020/12/21
    0)  release version
    1)  remove yellow bang state during driver updating process

Ver 9.2.0.0 - 2020/11/30
    0)  release version
    1)  support Windows 10 version 20H2
    2)  support Windows Server 2019

Ver 9.1.0.0 - 2020/09/16
    0)  release version
    1)  fix a COM port sequence problem after driver updating

Ver 9.0.9.0 - 2020/07/31
    0)  release version
    1)  fix Windows Update publish fail problem

Ver 9.0.8.0 - 2020/06/15
    0)  release version
    1)  fix a COM port property sheet issue

Ver 9.0.7.0 - 2020/05/20
    0)  release version
    1)  support Windows 10 version 2004

Ver 9.0.6.0 - 2019/11/22
    0)  release version
    1)  support Windows 10 version 1909

Ver 9.0.5.0 - 2019/05/21
    0)  release version
    1)  support Windows 10 version 1903

Ver 9.0.4.0 - 2018/10/09
    0)  release version
    1)  support Windows 10 version 1809

Ver 9.0.3.0 - 2018/05/22
    0)  release version
    1)  support Windows 10 version 1803

Ver 9.0.2.0 - 2018/04/25
    0)  release version
    1)  fix a system eventlog problem

Ver 9.0.1.0 - 2018/04/06
    0)  release version
    1)  fix a system eventlog problem

Ver 9.0.0.0 - 2017/12/25
    0)  release version
    1)  separate Win10 driver from legacy driver
    2)  fix an memory allocate problem

Ver 8.3.0.0 - 2017/10/23
    0)  release version
    1)  support Windows 10 version 1709
    2)  support Microsoft Declarative driver spec

Ver 8.2.3.0 - 2017/04/21
    0)  release version
    1)  support Windows 10 version 1703
    2)  fix a control sheet UI issue

Ver 8.2.2.0 - 2016/10/15
    0)  release version
    1)  support Windows 10 version 1607
    2)  modify control sheet UI

Ver 8.2.1.0 - 2016/05/24
    0)  release version
    1)  support more languages (add: Czech, French(Canada), Greek, Hebrew,
         Hungarian, Polish, Portuguese(Brazil), Russian, Slovak, Thai, Turkish)
    2)  remove COM baud rate offset error check
    3)  modify LPT driver interrupt method

Ver 8.2.0.0 - 2015/12/08
    0)  release version
    1)  modify driver to support specific platform
    2)  modify control sheet UI

Ver 8.1.5.0 - 2015/05/04
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
