==========================================================================================
=                                                                                        =
=             SUNIX PCI/PCI-104/PC-104/ISA I/O Board Driver Installation Guide           =
=                                                                                        =
=                                  For Windows CE 4.2                                    =
=                                                                                        =
=                                                               Version: 1.1.0.0         =
=                                                               Date: 2010/03/08         =
==========================================================================================

Item

A. Release note

B. Introduction

C. How to use SUNIX driver
   C.1	Driver installation
   C.2	Add driver into Platform Design
   C.3	Change COM port number
	
D. Utility
   D.1  snxdump


==========================================================================================

A. Release note

	Support x86 base cpu only.
	
	2009/02/20 - Ver:1.0.0.0
		1) Release driver

	2010/03/08 - Ver:1.1.0.0
		1) Support golden / matrix / SUN1999 series
		2) Support ISA card with IRQ sharing 
		3) Support PC-104/ISA series

		
------------------------------------------------------------------------------------------

B. Introduction

	Maximum 1 boards can be installed, support SUNIX PCI/PCI-104/PC-104/ISA I/O Board as 
	list below.


	1S -
		4027T       4027A       4027AL      4027D       4027DL      4027P
		5027A	    5027AL	5027H       5027HL      5027P       5027PL
		5027PH      5027PHL


	2S -
		4037T       4037A       4037AL      4037D       4037U       4037P
		4037PL
		8139        8139S       8139SI
		P1002       P2002       B1002       B2002
		4233A
		5037A       5037H       5037AL      5037HL      5037P       5037PH
                5037PL	   5037PHL
		
		
	4S -
		4056A       4056A3      4056A4      4056AL      4056D       4056J
		4056U       4056UE      4056P       4056PL      4056PM      4055WN
		4056DW      4056AM      4056LM      4056LL      4056JM      4056LV
		4000A       4000AL      4000P       4000PL	
		8159        8159S       8159SI
		P1004       P2004       P3004       B1004       B2004
		5056A	    5056AL	5056H	    5056HL      5056P       5056PL
                5056PH      5056PHL	5056U  	    5056UL	5056UH      5056UHL
		4243A
		IPC-A1004	
		
	8S -
		4066R       4066U       4066UE      4066WM      4066RM      4066JM
		8000A       8000AL	
		8169        8169S       8169SI
		P1008       P2008
		5066A       5066H       5066AL      5066HL      5066U       5066UL
		5066UH      5066UHL				
		

------------------------------------------------------------------------------------------

C. Driver installation

	C.1 Driver installation
		step 1.  please double click "SUNIX WinCE 4.2 Driver Vx.x.x.x.msi"
		step 2.  driver will install in C:\PLATFORM\Sunix_WinCE42\
		step 3.  finish driver install wizard


	C.2 Add driver into Platform Design
		step 1.  create a new platform design
		step 2.  select a BSP
		step 3.  select a design templates
		step 4.  in Platform Builder, select "Tools" and then select "CEC Editor"
		step 5.  in CEC Editor, select "File" and select "Open" to open cec file in 
                         C:\PLATFORM\Sunix_WinCE42\
                         if OS design build in debug mode, please open "sunixdbg.cec"
                         if OS design build in release mode, please open "sunixrtl.cec"
                         sunixdbg.cec will print debug informations in Debug window. If meet 
                         problem when development, please sent debug message to SUNIX.
			
		step 6.  after "sunixdbg.cec" opened, select "Catalog" and then select "Add to Catalog"
		step 7.  in Platform Builder, select "View" and then select "Catalog"
		step 8.  in Catalog window, click mouse right button and select "Refresh Catalog"
		step 9.  "sunix driver rtl" will show in \Third Party\SUNIX\, please click mouse right 
		         button and select "Add to Platform"
		         
		step 10. use "Build Platform" to build OS image.			         
					
		step 11. if want to remove driver, please delete "sunix driver dbg" in "FeatureView" and
		         build again.							
			
			
	C.2 Change COM port number	
		step 1.	 use text editor to open "snxcard.reg" in C:\PLATFORM\Sunix_WinCE42\	
		step 2.  change "Index" value to 1 ~ 9 to become COM1 ~ COM9,
                         please don't have a conflict with COM port number in 
                         target device board.


------------------------------------------------------------------------------------------

D. Utility

	D1. snxdump - dump port informations
	
		step 1.	please download or copy snxdump.exe (C:\PLATFORM\Sunix_WinCE42\App\) 
			to target device
			
		step 2. execute snxdump.exe in target device

			the informations should be like this


			COM5 - port:1, iobase:xEF00, irq:10, sysintr:32
							
			COM6 - port:2, iobase:xEF08, irq:10, sysintr:33
							
			Total found 2 SUNIX Port


------------------------------------------------------------------------------------------

