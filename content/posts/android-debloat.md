+++
title = "Android Debloat"
date = "2021-01-16T15:20:32+05:30"
author = "Pranav Kulkarni"
authorTwitter = "gamerhat18" #do not include @
cover = ""
tags = ["Android", "Debloat"]
keywords = ["Android", "debloat"]
description = "An easy guide for android-debloat project"
showFullContent = false
draft = false
+++


## You can check out the project [here](https://github.com/gamerhat18/android-debloat).

The main goal of this project is to improve battery-life and privacy by removing bloatware. The script has a menu that lets you choose what debloat list you want to use. I strongly encourage you to take a look at the lists because the default selection might not suit you. Almost all packages are documented in order to avoid mishappenings.

>`Tip:`
>You can always FACTORY RESET your phone if in case something goes wrong! So please make a Backup of everything.

>`Note:`
>
>This script is safe with the default options. The worse case scenario is an essential service failing to load during boot, causing a reboot. After about 5 failed system reboots, the phone boots into recovery mode & you will have to perform a FACTORY RESET. So backup your data. 


## You can:
* [X] `Quick search` all the packages in your phone
* [X] `Uninstall` or `Reinstall` system/user packages (manually or with the debloat lists)
* [X] ADB backup/restore (Limited functionality, see the [FAQ](https://github.com/gamerhat18/android-debloat/wiki/FAQ#there-is-no-debloat-list-for-my-phones-brand-can-you-add-it-))
* [X] Device brand detection and auto-selection of the appropriate manufacturer debloat list
* [X] Logs in `debloated_packages.txt` and `remaining_packages.txt`.
* [ ] Installation of alternative open-source apps replacing stock apps [***Coming Soon***]

## Brand Debloat lists 
* [X] Asus
* [X] LG
* [X] Google
* [X] Huawei
* [X] Motorola
* [X] Nokia
* [X] OnePlus
* [X] Oppo
* [X] Realme
* [X] Samsung
* [X] Sony
* [X] Xiaomi
* [ ] More coming soon...
## Universal Debloat lists 
* [X] AOSP
* [X] Google
* [X] Microsoft
* [X] Amazon
* [X] Facebook
* [X] Microsoft
* [X] Manufacturers (OEMs)
* [X] Mobile carriers
* [X] Qualcomm / MediaTek

## How to use?
> Step 1:
> **First Read the [FAQ](https://github.com/gamerhat18/android-debloat/wiki/FAQ)!**

> Step 2: 
> **Do a proper backup of your data! You can never be too careful!**

> Step 3:
> Enable `Developer Options` on your smartphone.
>
> Enable `USB Debugging` from the Developer Options.
>
> From the settings, logout from any OEM account (Like Samsung or Mi account). You can login back after you're done.
>
> Connect your phone to your Computer via USB, and click allow. Make sure you check the box first for the sake of convenience.
>
> ![*USB Debugging Prompt image*](https://raw.githubusercontent.com/gamerhat18/cybrdise-blog-hugo/master/content/posts/images/adbprompt.png)


4> Yes this is ToDo. 


### Install Dependencies
<p>
<details>
<summary>Linux</summary>

- Install ***Android platform tools*** and ***qpdf*** on your PC :

Debian Base :
```bash
$ sudo apt install android-sdk-platform-tools qpdf
```
Arch-Linux Base :
```bash
$ sudo pacman -S android-tools qpdf
```
Fedora :
```bash
$ sudo yum install android-tools qpdf
```
</details>
</p>

<p>
<details>
<summary>Mac OS</summary>

- Install [Homebrew](https://brew.sh/)
- Install *Android platform tools* and *qpdf*

You will also need to upgrade bash because Apple ships a very old bash version (3.2.57) due to licencing issues.

```bash
$ brew install android-platform-tools qpdf bash
```

You have to make the new bash version your default : 

```bash
$ sudo echo "/usr/local/bin/bash" >> /etc/shells
$ chsh -s /usr/local/bin/bash
```
Check if it works : 

```bash
$ echo $BASH_VERSION
```
</details>
</p>

<p>
<details>
<summary>Windows</summary>

You will need Chocolatey to install Git and ADB Platform Tools from Google.

```powershell 
choco install adb git -y
```

</details>
</p>

## Using on Windows
<p>
<details>
<summary>One-Step Process</summary>


Right click on the Start Menu and click on Windows Powershell (Admin). Click YES if something pops up. Then wait for a few seconds for it to load and paste the following. 
```powershell 
iex ((New-Object System.Net.WebClient).DownloadString('https://git.io/JtvK5'))
```

That's it! It will run the script program and you will have the control over enabling/disabling packages, restoring and creating backups, and more!
</details>
</p>

<p>
<details>
<summary>Manual Process</summary>

- Install the dependencies [mentioned above](https://github.com/gamerhat18/android-debloat/#install-dependencies)
- Clone this Repository.
- Browse through the debloat lists to be sure the default selection suits you.
- Run `debloat_script.sh` from the Git Terminal 
</details>
</p>

<p>
<details>
<summary>Using WSL (Not Recommended)</summary>


For now, there is no USB support in the WSL. This means you need to install both Windows and Linux platform-tools and force the use of Windows adb server.
- Download [android platform tools](https://dl.google.com/android/repository/platform-tools-latest-windows.zip) and unzip it somewhere. [Add the folder to your PATH](https://www.architectryan.com/2018/03/17/add-to-the-path-on-windows-10/).
- [Install USB drivers of your device](https://developer.android.com/studio/run/oem-usb#Drivers)
- Check your device is detected :
```batch
> adb devices
```

- Install [WSL2 (Windows Subsystem for Linux)](https://itsfoss.com/install-bash-on-windows/) in order to be able to run bash scripts.
- Install *Android platform tools* and *qpdf* from the Debian/Ubuntu shell
```bash
$ sudo apt update && sudo apt upgrade
$ sudo apt install android-sdk-platform-tools qpdf
```
- Check the version of ADB on Linux & Windows
```bash
adb version
```
You need the same version otherwise it will not work. It's very likely your Ubuntu/Debian ADB version is older than the Windows one. 
Download the lastest linux platform tools from Google & replace your adb binaries with the new ones :
```bash
$ wget https://dl.google.com/android/repository/platform-tools-latest-linux.zip
$ unzip platform-tools-latest-linux.zip
$ sudo cp platform-tools/adb /usr/bin/adb
$ sudo chmod 755 /usr/bin/adb
$ adb version
```
Kill the WSL adb server:
```bash
$ adb kill-server
```
And start the ADB server on Windows: 
```batch
> adb kill-server
> adb start-server
> adb devices
```
Note: You can access your Windows files under `/mnt/c/`

</details>
</p>


## Using on any Unix based system

<p>
<details>
<summary>Linux One-Step Process</summary>

- Open the terminal application.
- Copy and paste the following in the terminal and wait for it.
```bash 
curl -sSL https://git.io/JtfRu | bash
```
</details>
</p>


<p>
<details>
<summary>MacOS One-Step Process</summary>

- Open the terminal application.
- Copy and paste the following in the terminal and wait for it.
```bash 
curl -sSL https://git.io/JtfRB | bash
```
</details>
</p>

## Manual Process
- Install the dependencies [mentioned above](https://github.com/gamerhat18/android-debloat/#install-dependencies)
- Clone this Repository.
- Browse through the debloat lists to be sure the default selection suits you.
- Run `debloat_script.sh` from a Unix terminal 


**NOTE:** Chinese phones users may need to use the AOSP list for removing some stock apps because those chinese manufacturers (especially Xiaomi and Huawei) have been using the name of AOSP packages for their own (modified & closed-source) apps.

**IMPORTANT NOTE:** You will have to run this script whenever your OEM push an update to your phone as some *uninstalled* system apps could be reinstalled.

## How to contribute

Hey-hey-hey! Don't go away so fast! This is a community project. That means I need you! I'm sure you want to make this project better anyway.

==> [How to contribute](https://github.com/gamerhat18/android-debloat/tree/master/Contribute)