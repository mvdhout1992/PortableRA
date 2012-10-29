
                     COMMAND & CONQUER: RED ALERT

    Copyright (c) 1996 WESTWOOD STUDIOS, INC. All rights reserved

          Command & Conquer, Command & Conquer: Red Alert and
      Westwood Studios are trademarks of Westwood Studios, Inc.

                           November 9 1996

     For latest goodies, news and updates visit WWW.WESTWOOD.COM

 ============================================================================

 Contents:

 1. DOS

    1.1. Autodetection of Sound Cards

    1.2. Sound Card Troubleshooting

         1.2.1. Creative Labs - Soundblaster 1.0/1.5 card
         1.2.2. Soundblaster Compatible Cards
         1.2.3. Compaq Computers
         1.2.4. Sound Galaxy Basic 16
         1.2.5. ESS AudioDrive
         1.2.6. Adlib Gold
         1.2.7. Golden Sound Pro 16
         1.2.8. Gravis Ultrasound

    1.3. Modem Play

         1.3.1. Initialization Strings
         1.3.2. Modem Performance Hints
         1.3.3. 486 Machines With External Modems
         1.3.4. Plug and Play Modems
         1.3.5. Modem initialization problems
																												 
    1.4. Network Play

         1.4.1. Homogeneous Environment
         1.4.2. MSIPX.COM

 2. DOS box under Windows 95

    2.1. Running C&C:RA in a Windows 95 DOS box

    2.2. Improving movie playback performance

    2.3. Autodetecting Soundcards in a Windows 95 DOS box

    2.4. Microsoft Natural Keyboard

    2.5. Running DOS setup

 3. Windows 3.XX

    3.1. Launching C&C:RA

    3.2. Westwood Chat

 4. Windows 95

    4.1. Microsoft DirectX

    4.2. Known video card problems

         4.2.1. S3 TRIO video cards
         4.2.2. Screen distorts after installing Microsoft DirectX
         4.2.3. Unable to allocate primary video buffer

    4.3. Network Drivers

         4.3.1. Novell Client32
         4.3.2. THIPX32 DLL

    4.4. Uninstalling Red Alert

    4.5. Virtual Memory Settings

    4.6. Microsoft PowerToys

 5. General Troubleshooting

    5.1. CD-changers and multi-drives

    5.2. Microsoft Home Mouse and Natural Keyboard

 6. Game updates and patches

 7. General Gameplay Information
  
   7.1. Multiplay Notes

        7.1.1. Multiplay Tech Levels
        7.1.2. Multiplay Map Size Descriptions

 ============================================================================
 
 1. DOS

   1.1. Autodetection of Sound Cards
     
     The DOS version of C&C:RA will attempt to autodetect your sound card.
     Because of the vast number of machine configurations possible on PC's,
     C&C:RA may not autodetect your sound card correctly. For this reason
     you should treat the detected card as a suggestion only. If you know
     that the detected card is definitely wrong you can override the
     selection and pick the correct card from the SETUP program.
 
     If you select a sound card that is not present in your machine, your 
     machine may lock-up, or the sound card may stop responding. Either of
     these situations may be corrected by simply turning off the computer,
     waiting 15 seconds and then turning it back on.

   1.2. Sound Card Troubleshooting

     Here are some hints and tips for specific sound cards found
     while testing C&C:RA under DOS.

       1.2.1. Creative Labs - Soundblaster 1.0/1.5 card

         These early Soundblaster cards do not support some of
         the features which are built into later versions of the
         card. This may result in lower audio quality on
         these cards.
 
       1.2.2. Soundblaster Compatible Cards
    
         The Soundblaster code in C&C:RA is written for 100%
         Soundblaster compatible sound cards made by Creative Labs.
         If you have a Soundblaster compatible sound card from
         another manufacturer you may experience stuttering or
         popping in the sound, or even no sound at all.
 
         If you are unsure of the correct Port, IRQ and DMA settings
         for your Soundblaster compatible card, try typing SET from
         the DOS prompt. If your machine has been configured with a
         BLASTER environment variable in your AUTOEXEC.BAT file you
         should see a line similar to:
 
         SET BLASTER=A220 I5 D1 H5 T4
 
         The number after the A (i.e., 220 in this case) is your port
         address; the number after the I (5 in this case) is your IRQ
         and the number after the D (1 in this case) is your DMA channel
         setting. Armed with these numbers you can go ahead and manually
         select your soundcard from the SETUP program and enter the Port,
         IRQ and DMA in the boxes when prompted. If you have a Soundblaster
         16 or AWE32 soundcard and you are having difficulty with
         autodetection, these same comments apply except that you may
         have to enter the number after the H as your DMA setting,
         depending on your configuration.
 
       1.2.3. Compaq Computers

         Some Compaq machines may not autodetect the installed sound
         card.  If this occurs, try selecting Sound Blaster Pro/Pro2
         from the SETUP program.
 
       1.2.4. Sound Galaxy Basic 16
   
         This Soundblaster compatible card can sometimes be incorrectly
         autodetected as a Soundblaster Pro or Soundblaster 16, causing
         unpredictable results. We recommend that you manually select
         Soundblaster and enter the Port, IRQ and DMA values that
         correspond to your card. See the comments under Soundblaster
         compatible cards above.
     
       1.2.5. ESS AudioDrive

         Under certain circumstances the autodetect code can incorrectly
         identify this card as a Soundblaster 16. If this occurs you will
         need to override this driver by selecting ESS AudioDrive with
         the correct values for your system.
  
       1.2.6. Adlib Gold

         Under certain circumstances the autodetect code can return
         incorrect Port, IRQ and DMA settings. If you are having difficulty
         obtaining sounds on this sound card try manually selecting the
         card in the SETUP program and entering the correct Port, IRQ and
         DMA settings.

       1.2.7. Golden Sound Pro 16

         We have found that better results may be obtained on this
         sound card by reducing the game volume from the in-game
         sound control menu. Volume levels should be set to about
         half way.
 
       1.2.8. Gravis Ultrasound

         Some Gravis Ultrasound owners may experience audio clipping
         and/or reduced game performance.  We recommend that you turn
         the volume for musical scores all the way down (off) to see
         if this helps.

   1.3. Modem Play

     1.3.1. Initialization Strings

       We get best modem performance with modem data-compression
       and error-correction turned off. You can do this by going
       to the serial game settings dialog and entering the appropriate
       initialization string for your modem. This should be entered on
       the host (dialing) machine, the guest (receiver) should use ATZ.
       If you use these init strings the modem speed may have to be set
       to the exact speed of your modem, for example 14400 bps or 28800
       bps. Here are example init. strings for some popular modems:
 
       Modem                                        Init. String
                                              
       US ROBOTICS SPORTSTER 9600/14400/28800 . . . AT&M0&K0
       DIGICOM SCOUT 288VFCi  . . . . . . . . . . . AT\N1
       BEST DATA SMART ONE 14400  . . . . . . . . . AT\N1
       HAYES ACCURA 28800 . . . . . . . . . . . . . AT&Q0
       SUPRA 14400  . . . . . . . . . . . . . . . . AT\N1
       PRACTICAL 14400  . . . . . . . . . . . . . . AT&Q0
       ZOOM 28800 . . . . . . . . . . . . . . . . . AT&Q0

     1.3.2. Modem Performance Hints

       With music playing during a modem game, there is a possibility
       of pausing or very slow game play. For optimum performance, 
       music volume under the options menu should be set to zero 
       (far left), this is the default setting. The game speed should
       be satisfactory with sound effects on and music set to zero.
 
     1.3.3. 486 Machines With External Modems

       If you have a 486 system with an external modem you might
       experience pausing or very slow game play. This is due to
       the 8250 UART chip which is in most 486 class machines, this
       chip causes the CPU to work harder in null modem and modem
       games. There are several work-arounds: 
         
       1. Turn off both music and sound effects in the setup program 
       prior to playing the game. This will improves performance at
       the expense of losing all game sounds. 
         
       2. Install an internal modem. These modems have their own
       UART chips which are designed for higher performance.
 
       3. Install a high performance serial card in your system.
       If you are using a 14400 or 28800 bps external modem with 
       your 486 class system you should seriously consider installing
       a high performance serial card. These cards usually have a 
       16550A type UART chip which outperforms the 8250 UART in all 
       serial communications applications by buffering data more
       efficiently. 

     1.3.4. Plug and Play Modems

       Certain Plug and Play modems require a Plug and Play device
       manager to be installed before they will function under DOS.
       One source for such Plug and Play managers is Intel's WWW
       site at www.intel.com. Failing this you should contact your
       modem manufacturer for updated driver information.

     1.3.5. Modem initialization problems

       If you encounter errors while initializing your modem
       (for example the message, "Cannot disable modem
       auto-answer") make sure that the modem speed is set to
       an appropriate value.

   1.4. Network Play

     1.4.1 Homogeneous Environment

       For multiplayer network games we strongly caution you to use a
       homogeneous network environment - that is, to use the same type 
       of IPX compliant network drivers (e.g., IPX, IPXODI etc.) on each
       system. We have found incompatibilities between drivers from
       different manufacturers so you should bear this in mind if you
       are having network game troubles.
 
     1.4.2 MSIPX.COM

       C&C:RA should work with any IPX compliant network but we have
       found problems running with Microsoft MSIPX.COM. We strongly
       recommend that you avoid MSIPX and use either IPX.COM from Novell,
       or use IPXODI drivers compatible with your card. If in doubt you
       should ask your network administrator to upgrade your system.

 ============================================================================

 2. DOS box under Windows 95

   2.1. Running C&C:RA in a Windows 95 DOS box

     The DOS version of C&C:RA will run as a DOS box process under
     Windows 95. This might be useful if:
    
     - You have a 486 class machine running Windows 95 and 
       performance of the Windows 95 version of C&C:RA is too
       slow in the native Windows 95 environment.
     
     - You do not have Microsoft DirectX compatible video drivers
       installed on your Windows 95 system.

     If you install C&C:RA in Windows 95 but wish to play the DOS
     version, the setup program will launch to set up the sound
     settings.
 
   2.2. Improving movie playback performance

     The performance of C&C:RA in a Windows 95 DOS box is slightly
     slower than in a real DOS environment. You may be able to improve 
     movie playback performance by going into the Windows 95 START
     menu and selecting SETTINGS\CONTROL PANEL, then double-click
     SYSTEM and click PERFORMANCE\FILE SYSTEM\CD-ROM. There is a menu
     here which allows you to enable read-ahead buffering of the
     CD (this seems to be disabled by default). Select the setting
     that matches your CD-ROM drive (2X, 4X etc.). You can also
     change the size of the buffer, usually the bigger this is
     the better the performance will be, although this does take
     away memory from the rest of the system.

   2.3. Autodetecting Soundcards in a Windows 95 DOS box:

     Because the Windows 95 DOS box is really just emulating
     DOS (Windows continues to run in the background) you may
     experience problems autodetecting your sound card in this
     mode. There are two things you can do to address this:
 
     1. Do not autodetect, but pick your soundcard manually and
        enter the correct PORT, DMA and IRQ settings, or
     2. Run through Windows 95 DOS mode.

   2.4. Microsoft Natural Keyboard

     This keyboard, and other keyboards which feature the
     "Windows Key", can cause problems when playing the DOS
     version of C&C:RA in a Windows 95 DOS box. When the
     Windows Key is pressed and then another key is pressed,
     the behavior is as if the Windows Key has never been
     released, causing further keystrokes to be ignored. The
     solution is simply to press the Windows Key again which
     will clear the depressed key state.

   2.5. Running DOS setup

     To run the DOS setup under Windows 95 (to change your
     sound card settings) you should first open an MS-DOS
     prompt, change to the drive where you installed C&C:RA,
     change to the directory where C&C:RA is installed (by
     default C:\WESTWOOD\REDALERT) and type SETUP.
     

 ============================================================================

 3. Windows 3.XX

     3.1. Launching C&C:RA

       C&C:RA uses special code to launch itself in the Windows 3.XX
       environment, and will attempt to close any active Windows applications
       prior to running. You will not be able to access other Windows
       programs when C&C:RA is active. Windows is automatically restarted
       when you exit C&C:RA.

     3.2. Westwood Chat

       To run Westwood Chat under Windows 3.XX, you must first ensure
       that Win32s version 1.3 or higher is installed on your system.
       Once you have Win32s installed, you should install Westwood Chat
       by selecting Run from the File menu, then select Setup.exe from
       the PlanetWW directory at the root of the CD. This will automatically
       install Westwood Chat on your drive.

       Please note that you will also need to have a Winsock 1.1 compliant
       TCP/IP stack and an account with an Internet Service Provider in
       order to run Westwood Chat.

       You cannot play C&C:RA over the Internet under Windows 3.XX, but
       you are able to chat with other C&C:RA players, as well as players
       of other Westwood Studios games.

 ============================================================================

 4. Windows 95

   4.1. Microsoft DirectX

     The Windows 95 version of C&C:RA is a Microsoft DirectX application.
     Version 3.0 of Microsoft DirectX is included on the CD and you have
     the option to install it when C&C:RA is installed.

     If you have difficulty running Windows 95 after these new
     Microsoft DirectX drivers have been installed, please contact
     your local Microsoft subsidiary, or write:

     Microsoft Customer Sales and Service,
     One Microsoft Way,
     Redmond, WA 98052-6399, USA

     USA telephone: 1-800-426-9400
     International telephone: ++1-206-882-8080

     All Microsoft DirectX drivers are located in the Dxsetup folder
     off of the root of the CD. To reinstall the Microsoft DirectX
     drivers go into the Dxsetup folder and run Dxsetup.exe. You can
     explore the CD by choosing the "Explore the CD" option in the
     autoplay title screen.

   4.2. Known video card problems

     Here are some hints and tips for specific video cards found
     while testing C&C:RA under Windows 95.

     4.2.1. S3 TRIO video cards

       We have noticed corruption on screen during both game and movies
       with some (but not all) examples of video cards with this chipset.
       There is no specific workaround but you should check with your
       video card manufacturer for updated driver information.

     4.2.2. Screen distorts after installing Microsoft DirectX

       We've found that video monitor settings may need to be
       adjusted after installing the Microsoft DirectX video drivers.
       If your screen distorts, or is shifted horizontally or vertically,
       you can return it to normality by adjusting the controls on your
       monitor. You should only need to do this once.

     4.2.3. Unable to allocate primary video buffer

       If you receive an "Unable to allocate primary video buffer
       - Aborting." error message try reinstalling the Microsoft DirectX
       drivers. If reinstalling the Microsoft DirectX drivers does not solve
       this problem, then that means that your video card manufacturer has
       not updated their video drivers to be Microsoft DirectX compliant.
       Call your video card manufacturer for updated drivers.

   4.3. Network Drivers

     Here are some hints and tips found during network game testing
     of C&C:RA for Windows 95.

     4.3.1. Novell Client32

       C&C:RA may not detect the presence of IPX drivers if you have
       installed Novell Client32 for Windows 95. There is currently
       no known workaround other than to reinstall the Microsoft
       IPX protocol which is shipped with Windows 95.

     4.3.2. THIPX32.DLL

       C&C:RA uses a custom DLL file for network play. If you see an
       error message which mentions "THIPX32.DLL", you should reboot
       your system and start C&C:RA again. If the problem persists,
       you may need to reinstall C&C:RA.

   4.4. Uninstalling Red Alert

     After running the Uninstall program, if the Red Alert group is
     still present, try rebooting your computer. This should clean up
     the Red Alert start menu folder.

   4.5. Virtual Memory Settings

     C&C:RA may need to use more RAM than is present on your system.
     Windows 95 automatically takes care of this by using what is
     known as "Virtual Memory" - it uses space on your hard disk
     to simulate the memory it needs and swaps data back and forth
     from your hard disk as required. Windows 95 allows you to manually 
     set the amount of hard drive space it uses for Virtual Memory:
     WE HIGHLY RECOMMEND THAT YOU DO NOT DO THIS! To let Windows 95
     manage the Virtual Memory, go to the Windows 95 START menu,
     select SETTINGS\CONTROL PANEL, then double-click SYSTEM, click
     PERFORMANCE\FILE SYSTEM\VIRTUAL MEMORY and then select "Let
     Windows manage my virtual memory settings (recommended)".

   4.6. Microsoft PowerToys

     If you have the Microsoft PowerToys system extensions installed
     on your system (including QuickRes and FlexiCD) you may experience
     a black screen upon booting C&C:RA, although the sounds may still
     be audible. If this happens, you should remove the MicroSoft
     PowerToys while playing C&C:RA.

 ============================================================================
 
 5. General Troubleshooting

   5.1. CD-changers and multi-drives

     C&C:RA does not support multiple CD-ROM drives or CD-changers and
     assumes that you only have one CD-ROM drive. If you have more than
     one CD-ROM drive, you should insert the C&C: Red Alert CD you are using
     into the first CD driver letter. For example, if you have drives E:, F:
     and G:, your C&C:RA CD should be inserted into the E: drive.
                     
   5.2. Microsoft Home Mouse and Natural Keyboard

     If you are using a Microsoft Home Mouse, the Microsoft Natural
     Keyboard or are using Microsoft's IntelliPoint Tools and
     Controls Software, having the "Sonar" setting on under "Visibility"
     in the "Mouse Properties" section in the "Control Panel" can cause
     C&C:RA to crash.  Please turn this setting off when playing
     C&C:RA.

 ============================================================================

 6. Game updates and patches

   If it becomes necessary to update your game, you can find game updates 
   on our web page at http://www.westwood.com or at our FTP site 
   (ftp.westwood.com). Please mail all questions to our internet mailing 
   address: mail@westwood.com

 ============================================================================

 7. General Gameplay Information
  
   7.1. Multiplay Notes

     7.1.1. Multiplay Tech Levels
     
     This chart shows what units, structures, and abilites become available
     at the various tech levels in multiplay.     
                                            
     TL Allied Unit    Allied Structure     Soviet Unit      Soviet Structure
     -- -----------    ----------------     -----------      ----------------
     1  Rifle Infantry Tent Barracks        Grenadier        Barracks
     1  Rocket Soldier Power Plant          Rifle Infantry   Power Plant
     1  Medic          Ore Processor        Rocket Soldier   Ore Processor
     1                 Ore Silo                              Ore Silo
     1                 Sandbag Wall                          Fence
     1                 Pillbox                               Flame Tower
     1                                                       Barbed Wire
    
     2  AT Mine Layer  Radar                AP Mine Layer    Radar
     2  Ranger         War Factory          Ore Truck        War Factory
     2  Ore Truck      Service Depot.       Transport        Service Depot.
     2  Transport      Camo Pillbox         Attack Dog       Kennel
     2  Light Tank     Naval Yard           Heavy Tank       Sub Pen 
     2  Turret                              V2 Rocket
                                             Launcher 
    
     3  PT Boat        AA gun               Yak              Airfield
     3  APC                                 Spy Plane* 
     3  Engineer                            Engineer 
     3                                      Submarine    
    
     4  Medium Tank    Sonar Pulse*         Flame-Thrower    Tech Center
     4  Spy                                  Soldier         Tesla Coil
     4  Destroyer   
    
     5  Artillery      Advanced Power       Parachute        Advanced Power
                        Plant                                 Plant
     5                 Concrete Wall        Bombs*           Concrete Wall
    
     6 Longbow Apache  Helipad              Hind             Helipad
     6                                                       SAM Site
    
     7 Cruiser         Tech Center          Mammoth Tank 
     7                 Gap Generator        MIG              
     7                 GPS Satellite*  
    
     8 MCV                                  MCV 
     8 Tanya                                Tanya 
     8 Thief                                Chinook 
     8 Mobile Gap
        Generator   
    
     9 Chronoshift*    Chronosphere         Invulnerability* Iron Curtain
     9 Mobile Radar 
        Jammer   
    
    10 Atomic Bomb*    Missile Silo         Atomic Bomb*     Missile Silo

    (* = This item is a special game ability.)

    7.1.2. Multiplay Map Size Descriptions

      When you go to choose a map to play on in multiplay, you will notice
      some characters at the end of each map name.

      SM  = Generally means a smaller map. Recommended for 2-4 players.
      MED = Generally means a medium sized map. Recommended for 4-6 players.
      LG  = Generally means a large map. Anywhere from 6-8 players can play
            on these maps.

      Any number of players (from 2-8) can play on any of these maps. The
      description is merely a recommendation.
