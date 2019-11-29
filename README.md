# gawa

Just want to download the latest APK?

<a id="raw-url" class="btn btn-sm BtnGroup-item" href="com.gawaproject.apk">Download APK</a>

[apk]("/jamesjohnmcguire/gawa/raw/master/com.gawaproject.apk")

Installing APK on an emulator

	1. Install an emulator
	There are many android emulators out there of varying quality.  I like genymotion.  You can find the installer here:
		dl.genymotion.com/releases/genymotion-2.8.1/genymotion-2.8.1.exe
	If you use genymotion, you will need to create at least one virtual phone.  You can do this by:
		a. Open GenyMotion
		b. Agree to whatever terms of service
		c. Click on the add button on the toolbar
		d. You may need to download some templates
		e. Choose a newer standard phone, Google Nexus 9 is a good choice. Try to target something that has an API version of 25.
	Victor introduced me to KO player, which also seems quite good.  You can find the installer here:
		http://www.koplayer.com/

	2. Download the APK
	Go to my GitHub site here:
		https://github.com/jamesjohnmcguire/gawa.git
	Click on the APK link (or use this: https://github.com/jamesjohnmcguire/gawa/blob/master/com.gawaproject.apk)
	Click the download button.  The file should be downloaded.

	3. Set Security Settings
	By default, Android doesn't allow installation of APK files outside of Google Store
	Open up your emulator.  Go through any dialogs or setup that may need to happen.
	Choose Settings -> Security -> Allow Unknown Sources
	Switch to On

	4. Install the APK
	Go to your downloads folder (or where the file was downloaded to).  Click on the APK file and simply, drag and drop it on to the emulator.  It should install itself just fine and icon with app should be in applications or the main screen.


Installing on the Phone

	They don't make this easy and this can get a bit technical.  I wouldn't be surprised if you run into problems, trying to do this the first time around.

	1. Enable Installation of external APK Files
		a. Allow Unknown Sources
			On your phone, choose Settings -> Security -> Allow Unknown Sources
			Switch to On
		b. Turn on Developer Options
			On some systems, the Developer options screen is hidden by default.
			On your phone, choose Settings
			Check to see if there is an option for Developer Options
			If so, continue to c.
			If not, go to Settings > About phone
			tap Build number seven times
			Return to the previous screen to find Developer options at the bottom.
			On some devices, the Developer options screen might be located or named differently.
		c. Enable USB debugging
			On your phone, choose Settings -> Developer -> USB Debugging
			Switch to On

	2. Install ADB (Android Debug Bridge)
		On your PC, download the Android Platform SDK Tools here:	https://dl.google.com/android/repository/platform-tools-latest-windows.zip
		Unzip the file and install to a folder of your choice.  Let's say C:\android

	3. Add ADB to your path
		On your PC, right-click on the Windows Start button (1st on the left bottom menu)
		Choose System from the menu
		On the new window, choose Advanced System Settings
		ON the new dialog that pops up, choose environment variables
		In the system variables list, choose Path, Edit
		Choose New
		In the space provided, type in the install location (e.g. C:\android)
		Press OK a few times and close those windows

	4. Connect your Phone to your PC
		Connect your phone to your PC with a USB cable
		Wait for the phone to show up on the screen of your computer (it may do so after install drivers)

	5. Run ADB
		On your PC, go to search (2nd icon on the left bottom menu), type cmd and choose 'Command Line'
		On the command line, type adb devices
		At this point, you should see your phone listed

	6. Install the APK
		On the command line, type: cd %USERPROFILE%\downloads (or where you downloaded the APK to)
		cross your fingers
		type: adb install com.gawaproject.apk
		If all goes well, the application should be on your phone

	Some additional help
		https://developer.android.com/studio/command-line/adb.html#move
