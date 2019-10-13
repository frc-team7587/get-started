# Environment Setup
A set of software components must be installed on the laptop, which is to be the Driver Station of your robot. Make sure you have a stable and decent Internet connection.

## FRC Update Suite by NI ([National Instruments](http://www.ni.com))
NI software provides the Driver Station and tools for imaging the roboRIO, which is the brain that operates the robot. Instead of repeating the instruction, following below WPI instruction to download and install the suite.

1. Go to http://www.ni.com/download/first-robotics-software-2017/7904/en/, and click the link **FRCUpdateSuite_2019.2.0.zip**.
2. You'll be prompted to log in, create an account if needed.
3. After downloaded, unzip the zip file to a local folder, go into the folder and double-click **setup.exe** to start installation.

On most of the installation wizard screens you click "Next" to move along. Pay attention to a few screens below:

![WPILib Installer Icons](img/ni3.JPG)

Enter Team7587's license activation code **B04P65237** on this window:

![WPILib Installer Icons](img/ni4.JPG)

Ensure to accept 2 license agreements:

![WPILib Installer Icons](img/ni5.JPG)

![WPILib Installer Icons](img/ni6.JPG)

Note the warning on Windows firewall, and make sure you pick "Allow Access" whenever prompted:

![WPILib Installer Icons](img/ni8.JPG)

**IMPORTANT:** Make sure you tick the checkbox to run license manager at the end of installation:

![WPILib Installer Icons](img/ni9.JPG)

When license manager starts, if you already logged in on the ni.com site, it's most likely that the serial number you entered above is already populated; if not, just enter it again, then click the 'Activate' button:

![WPILib Installer Icons](img/ni11.JPG)

After activating the license, restart the laptop as prompted. After reboot, you should see below three tools on your desktop:

* Driver Station
* FRC Dashboard
* roboRIO Imaging Tool

![WPILib Installer Icons](img/dsinstall.PNG)

### Driver Station
The Driver Station (DS) is a critical part of your robot software. It is the user interface on your laptop that enables you to communicate with the robot, and **drive** it. Now you should launch the DS and inspect its various components.

By default, DS launches itself plus the default Dashboard:

![Driver Station](img/ds.PNG)

Read the article [FRC Driver Station](https://wpilib.screenstepslive.com/s/currentCS/m/driver_station/c/86704) as you move along.

~~~
Tip: Connect your joystick and game pad to the laptop and see if DS detects them.
~~~  

## FRC Development Tools by WPI
In 2019 WPI deprecated Eclipse and started pushing **Visual Studio Code** (a light-weight development tool by [Microsoft](https://code.visualstudio.com/)) as the new standard IDE. A single "one-stop-shop" installer replaces previous multi-step manual process, and takes care of all the software pieces needed for programming.
>**Note:** The WPI package installer contains a specific JDK version (v11), do not use any JDK outside of the installed package.

1. Go to [https://github.com/wpilibsuite/allwpilib/releases](https://github.com/wpilibsuite/allwpilib/releases) to download the latest version; at this point it's either **WPILibInstaller_Windows64-2019.4.1.zip** (for 64-bit Windows) or **WPILibInstaller_Windows32-2019.4.1.zip** (for 32-bit Windows). The file is close to 1 GB, it will take some time. Save the downloaded file to a local folder.

>To determine your Windows version, go to **Control Panel** and open **System**, look for "System type" field.

2. The downloaded zip file contains only a single file with same name but .exe file extension, extract it to a the same folder, double-click it to start the installation. To extract the file, right-click it and choose 'Extract All'.

3. The installer will initially have the two checkboxes "Visual Studio Code" and "Visual Studio Code Extensions" disabled (see below). You need to click "Select/Download VS Code" button to download it first. The downloaded file is **OfflineVsCodeFiles-1.3x.1.zip** and will be placed in the same folder as the installer. Leave it there and don't open it.

![WPILib Installer VSCode](https://raw.githubusercontent.com/team7587/FRC2019/master/resources/img/wpilib-install-vscode.PNG)

4. Back on WPILib Installer, check the two "Visual Studio Code..." checkboxes, and click "Execute Install" to start the full installation process. After a while you'll get a prompt confirming the installation is completed, and see below 3 icons placed on the desktop.

![WPILib Installer Done](https://s3.amazonaws.com/screensteps_live/image_assets/assets/002/027/165/original/908ac47e-8564-4119-988c-39fb30fe7389.png)

![WPILib Installer Icons](https://raw.githubusercontent.com/team7587/FRC2019/master/resources/img/wpilib-install-done.PNG)

5. Double-click the icon "FRC VS Code 2019" to launch the IDE, type **Ctrl+Shift+P**. A command pallet shows up on the top, type in "WPILIb" and you should see a list of WPILib commands show up. This confirms that the installation is successful.

![WPILib Installer Icons](https://raw.githubusercontent.com/team7587/FRC2019/master/resources/img/vscode-wpilib-cmdpalet.png)

>**Note:** The installation places all the files in the folder **C:\Users\Public\frc2019**, this way all users on the laptop can access them.

### 3. Phoenix Framework by CTRE ([Cross The Road Electronics](http://www.ctr-electronics.com/))
In order to use the **Talon SRX** motor controller, the **Phoenix Software Package** from its manufacturer CTRE is required. Installation is straightforward:
1. Visit http://www.ctr-electronics.com/hro.html#product_tabs_technical_resources
2. Click the link **CTRE Phoenix Framework Installer 5.15.0.1 (.zip)** to download the zip package
3. The zip file contains a single file with same name but .exe extension, extract it out to local folder
4. Double-click it to start the installation (it will require admin rights)
5. If you see below alert window, click 'Install' to continue:

![WPILib Installer Icons](img/ctre-alert.PNG)

After installation completes, the Phoenix Tuner icon shows up on your desktop:

![WPILib Installer Icons](img/phoniex1.PNG)

Launch the tuner and it would look like this:

![WPILib Installer Icons](https://raw.githubusercontent.com/team7587/Knowledge-Base/master/media/img/phoenix-tuner.PNG)

> More information on Phoenix Software can be found [here](https://phoenix-documentation.readthedocs.io/en/latest/ch03_PrimerPhoenixSoft.html#what-is-phoenix-tuner).
>

Now that your environment is up, let's move on to take a closer look at the basics of robot programming.
