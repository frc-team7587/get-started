**Welcome to Team7587 and the exciting world of FRC robot programming!**

This document aims to help team members who are new to FRC robot programming to get started.

# Knowledge Prep

It is probably **OK** if you want to skip this part and get to the hands-on steps below to get things going. However, there are a few fundamental concepts you should get familiar with, so make sure you come back and work on this section soon.

First thing first, bookmark this website **FRC 2019 Control System** [https://wpilib.screenstepslive.com/s/currentCS](https://wpilib.screenstepslive.com/s/currentCS)

WPI ([Worcester Polytechnic Institute](https://www.wpi.edu/)) is the owner of **WPILib**, a collection of tools, libraries and development guides that allow FRC teams write software for their robots.

>**Note:** This guide assumes you have basic knowledge of Java programming language.

### Important Reads:
1. [FRC Control System Hardware Overview](https://wpilib.screenstepslive.com/s/currentCS/m/cs_hardware/l/144968-frc-control-system-hardware-overview) - it's necessary to know the basic hardware components so we understand the context of our code (i.e. what code is for which hardware part).

2. [FRC Software Component Overview](https://wpilib.screenstepslive.com/s/currentCS/m/getting_started/l/144981-frc-software-component-overview) - get an overview of supported OS, programming language, IDE, and essential monitoring & testing tools.

## Laptop

Bring a laptop computer with:

* Intel Core i5/7 CPU, minimum 8GB memory and 256 GB storage 
* 3 USB ports, Wifi 
* Built-in Ethernet port (highly desirable) 
* Class A-B USB cable 
* Ethernet cable 
* A local account (not Microsoft account) with admin rights (i.e. in the Administrators group) 
* Windows 8/10 
* Chrome browser

**IMPORTANT:** Remove any anti-virus software such as McCafee or Norton, [disable Windows Defender](https://www.wikihow.com/Turn-Off-Windows-Defender-in-Windows-10), and [turn off automatic Windows Update](https://www.windowscentral.com/how-stop-updates-installing-automatically-windows-10).

## NI Account
The software from National Instruments (NI) requires login for download, you'll need to create an account on [ni.com](ni.com). The account is also required for license activation.

## git
**git** is the bread-and-butter of any serious programming work. If you are new to git, get it and learn it at https://git-scm.com/.

## GitHub Account
You may be able to go through this guide without it, but you'll need your GitHub account to work with your team mates developing the robot code. Just create one on [github.com](https://github.com) now if you still don't have it.

# Environment Setup
A set of software components must be installed on the laptop, which is to be the Driver Station of your robot. Make sure you have a stable and decent Internet connection.

## FRC Update Suite by NI ([National Instruments](http://www.ni.com))
NI software provides the Driver Station and tools for imaging the roboRIO, which is the brain that operates the robot. Instead of repeating the instruction, following below WPI instruction to download and install the suite.

1. Go to http://www.ni.com/download/first-robotics-software-2017/7904/en/, and click the link **FRCUpdateSuite_2019.2.0.zip**.
2. You'll be prompted to log in, create an account if needed.
3. After downloaded, unzip the zip file to a local folder, go into the folder and double-click **setup.exe** to start installation.

On most of the installation wizard screens you click "Next" to move along. Pay attention to a few screens below:

![WPILib Installer Icons](https://raw.githubusercontent.com/team7587/Knowledge-Base/master/resources/img/ni3.JPG)

Enter Team7587's license activation code **B04P65237** on this window:

![WPILib Installer Icons](https://raw.githubusercontent.com/team7587/Knowledge-Base/master/resources/img/ni4.JPG)

Ensure to accept 2 license agreements:

![WPILib Installer Icons](https://raw.githubusercontent.com/team7587/Knowledge-Base/master/resources/img/ni5.JPG)

![WPILib Installer Icons](https://raw.githubusercontent.com/team7587/Knowledge-Base/master/resources/img/ni6.JPG)

Note the warning on Windows firewall, and make sure you pick "Allow Access" whenever prompted:

![WPILib Installer Icons](https://raw.githubusercontent.com/team7587/Knowledge-Base/master/resources/img/ni8.JPG)

**IMPORTANT:** Make sure you tick the checkbox to run license manager at the end of installation:

![WPILib Installer Icons](https://raw.githubusercontent.com/team7587/Knowledge-Base/master/resources/img/ni9.JPG)

When license manager starts, if you already logged in on the ni.com site, it's most likely that the serial number you entered above is already populated; if not, just enter it again, then click the 'Activate' button:

![WPILib Installer Icons](https://raw.githubusercontent.com/team7587/Knowledge-Base/master/resources/img/ni11.JPG)

After activating the license, restart the laptop as prompted. After reboot, you should see two icons below on your desktop:

![WPILib Installer Icons](https://raw.githubusercontent.com/team7587/Knowledge-Base/master/resources/img/ni14.JPG)

That indicates the NI software has been installed successfully.

### Driver Station
The Driver Station (DS) is a critical part of your robot software. It is the user interface on your laptop that enables you to communicate with the robot, and **drive** it. Now you should launch the DS and inspect its various components.

Read the article [FRC Driver Station](https://wpilib.screenstepslive.com/s/currentCS/m/driver_station/c/86704) as you move along.

~~~
TIP: Connect your joystick and game pad to the laptop and see if DS detects them.
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

![WPILib Installer Icons](https://raw.githubusercontent.com/team7587/Knowledge-Base/master/resources/img/ctre-alert.PNG)

After installation completes, the Phoenix Tuner icon shows up on your desktop:

![WPILib Installer Icons](https://raw.githubusercontent.com/team7587/Knowledge-Base/master/resources/img/phoniex1.PNG)

Launch the tuner and it would look like this:

![WPILib Installer Icons](https://raw.githubusercontent.com/team7587/Knowledge-Base/master/media/img/phoenix-tuner.PNG)

> More information on Phoenix Software can be found [here](https://phoenix-documentation.readthedocs.io/en/latest/ch03_PrimerPhoenixSoft.html#what-is-phoenix-tuner).
>

Now that your environment is up, let's move on to take a closer look at the basics of robot programming.

# Basic Code Structure
Now it's time to dive a little deeper to robot programming. **How does the Java code of a robot look like?** Read a few pages on WPI site and you'll get a better understanding fairly quick:

### Layout
Read the explanation of the Java robot project code layout here: [https://wpilib.screenstepslive.com/s/currentCS/m/robotbuilder/l/292704-robotbuilder-created-code](
https://wpilib.screenstepslive.com/s/currentCS/m/robotbuilder/l/292704-robotbuilder-created-code).

>**Note:** You don't need to know about the RobotBuilder tool mentioned in the document. The goal is for you to write the robot code rather than relying on the RobotBuilder to create code for you.

### Command-based Programming
Visit the WPILib site chapter [FRC Java Programming](https://wpilib.screenstepslive.com/s/currentCS/m/java), expand the menu item "Command based programming" on the left to see sub-topics, read at least the first three topics.

### Base Robot Class
The base robot class determines the code structure and pattern used in your robot code. Read this article [Choosing a Base Class](https://wpilib.screenstepslive.com/s/currentCS/m/java/l/599697-choosing-a-base-class) to understand base robot coding patterns. You'll see that the recommended base robot class is **TimedRobot**.

>**Useful Resource**: Bookmark the [WPILib API](https://first.wpi.edu/FRC/roborio/release/docs/java/), you'll need it.

# roboRIO Setup
Just as you need to format and install a new OS on a blank hard drive, the roboRIO needs to be "initialized" via the process of imaging using NI's roboRio imaging tool.

### Imaging your roboRIO

(being written as we speak...)

### Verify Driver Station Connectivity

(coming soon...)

# Your First Robot Program

(coming soon...)

### Create Project in VSCode
(coming soon...)

###Deploy to roboRIO
(coming soon...)

### Go Robot!
(coming soon...)

