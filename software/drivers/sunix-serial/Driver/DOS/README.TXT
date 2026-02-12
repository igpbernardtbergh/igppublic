==========================================================================================
=                                                                                        =
= 			            	    SUNIX Card Board Driver Installation Guide   =
=                                                                                        =
= 		                                For DOS 6.22				 =
=                      Copyright 2014 SUNIX GROUP all right reserved                     =
=                                                               Version: 1.00.000.006    =
=                                                               Date: 2014/08/18	 =
==========================================================================================

Item

A. Release note

B. Remap Card Introduction 

C. CLK Relations

D. Command List

E. Example
==========================================================================================

A. Release note

	Support DOS 6.22 on x86 machine only. 
	2013/08/18 - Ver:1.00.000.006  support sun2000 clock 14.7456Mhz to stardand 1.8432Mhz 
	2013/06/15 - Ver:1.00.000.005  updata snxlib.lib to sun1999 10s1p card
	2012/12/11 - Ver:1.00.000.004  Add No BIOS Present message
	2012/06/26 - Ver:1.00.000.003  debug lpt mode set
	2010/05/24 - Ver:1.00.000.002  debug show onboard port set
	2009/10/26 - Ver:1.00.000.001  updata matrix 1016 card
	2009/12/31 - Ver:1.00.000.000  updata version


------------------------------------------------------------------------------------------

B. Remap Card Introduction

	PCI serial ports can support the remapping function  
	
	1 Serial Port -
		4027D	
	
	2 Serial Port -
		4037D

	4 Serial Port -
		4056D
	
	All PCI parallel ports are possible to be remapped to legacy I/O
  address (378h,278h)
  
	2 Serial Port And 1 Parallel Port -
		4079D
	
	1 Parallel Port -
		4008
		PAR5008
		
	2 Parallel Port -
		4018
		
	
  
------------------------------------------------------------------------------------------
 C. PCI serial card are drived by a higher CLK (14.7456 Mhz), 
      thus the actual baudarate is 8 times higher than the BIOS/DOS baudrate 
      setting. The below table shows the relation.


*** Clock=14.7456 Mhz for all non-remapable port  ***

      Item   Actual Baudrate    BIOS/DOS setting    Remark
      =====  ================   =================   ==================
       1       921600                    115200
       2       460800                     57600
       3       230400                     28800     Non BIOS standard
       4             115200               14400     Non BIOS standard
       5              57600                7200     Non BIOS standard
       6              38400                4800 
       7              19200                2400  
       8               9600                1200
       9               4800                 600     Non BIOS standard
      10               2400                 300
      11               1200                 150 
      12                300                37.5     Non BIOS standard

 *** Clock=1.8432 Mhz for remapable port in DOS ***

      Item   Actual Baudrate    BIOS/DOS setting    Remark
      =====  ================   =================   ==================
       1       921600                               Do not support
       2       460800                               Do not support
       3       230400                               Do not support                 
       4             115200              115200                         
       5              57600               57600                        
       6              38400               38400 
       7              19200               19200  
       8               9600                9600
       9               4800                4800                      
      10               2400                2400
      11               1200                1200 
      12                300                 300        
------------------------------------------------------------------------------------------
D. Command List

	-help/-? 	Show help massages.
	
	-sc				list card number for remaps and remapp use.
	
	-lpt			Seting parallel mode to spp,ecp,epp,pff,bpp
	
	-force		Designated address to lpt(com) number,login in the system. 
	
	-remaps		Remap address to available standard serial port address.
	
	-remapp		Remap address to available standard parallel port address.
	
	-freqdown	freq 14.7456MHz to standard 1.8432MHz SUN2000 CHIP Only.
	
------------------------------------------------------------------------------------------
E. Example  (4056D and 4008 and 6469A Card Test )

	*********SER4056D AND PAR4008 **************
	c:\>sundos -sc
	
	Sunix IO card Uti1ity for DOS ver.1.00.00.006
	--------Search All Cards--------
	1:0048	Serial:4	Parallel:0
	2:0058	Serial:0 	parallel:1
	
	c:\>sundos -remapp 2 278
	
	Sunix IO card Uti1ity for DOS ver.1.00.00.006
	Parallel Seting Address
	Parallel Port1 = 278H
	Extended Registers Address = 678H
	
	c:\>sundos -force 278 lpt2
	
	Sunix IO card Uti1ity for DOS ver.1.00.00.006
	Address 278H Seting To LPT2
	
	c:\>sundos -lpt2=spp
	
	Sunix IO card Uti1ity for DOS ver.1.00.00.006
	Seting LPT2 to spp
	
	c:\>sundos -remaps 1 3f8 2f8 3e8 2e8

	Sunix IO card Uti1ity for DOS ver.1.00.00.006
	4056D Seting Address
	Serial Port1 = 3f8H
	Serial Port2 = 2f8H
	Serial Port3 = 3e8H
	Serial Port4 = 2e8H
	
	c:\>sundos
	
	Sunix IO card Uti1ity for DOS ver.1.00.00.000	
	--------Sunix Card 4 Port Serial 0 Port Parallel--------
	Serial Port 1 Base Addr 		=	3f8H IRQ=9   COM1
	Serial Port 2 Base Addr 		=	2f8H IRQ=9   COM2
	Serial Port 3 Base Addr 		=	3e8H IRQ=9   COM3
	Serial Port 4 Base Addr 		=	2e8H IRQ=9   COM4
	--------Sunix Card 0 Port Serial 1 Port Parallel--------
	Parallel Port1 							= 278H IRQ=11  LPT2
	Extended Registers Address	= 678H
		
	c:\>

	****************SER6469A***************

	c:\>sundos -sc
	
	Sunix IO card Uti1ity for DOS ver.1.00.00.006
	--------Search All Cards--------
	1:0200	Serial:1	Parallel:1

	c:\>sundos -freqdown 1

	Sunix IO card Uti1ity for DOS ver.1.00.00.006
	SUN2000 Set ok!!!!!!

	c:\>



------------------------------------------------------------------------------------------

