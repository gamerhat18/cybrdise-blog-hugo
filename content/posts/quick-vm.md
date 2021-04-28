+++
title = "Quick VM Setup"
date = "2021-04-25T15:20:32+05:30"
author = "Pranav Kulkarni"
authorTwitter = "thegamerhat" #do not include @
cover = "" #
tags = ["VM", "Virtual", "Machine", "Virtual Machine", "ASAP"]
keywords = ["Linux", "Windows", "MacOS", "Mac OS", "Virtual Machine", "VM"]
description = "An easy and quick way to bring VMs to masses and help people to switch to Linux from Windows/MacOS."
showFullContent = false
draft = false
+++


# Quick-VM

Summary of the [Quick-VM Project](https://github.com/thegamerhat/quick-vm) on GitHub.

Windows 10 is used by many, in personal computers, enterprise, workstations, etc. Not because it is the best, nor because it is the fastest, or the most secure. Infact, quite the contrary as it is one of the most insecure and efficient.

## **Some of the practical problems including but not limited to:**

- **The latest windows update has even proved to be devastating for computers running Windows 10, as many users were stuck with a non-functioning computer altogether.**
    - [2021 Bootloop Bug](https://www.windowslatest.com/2021/04/21/april-2021-patch-is-now-causing-trouble-for-more-windows-10-users/)

- **Windows Deleting your important files without your consent, which happened twice.**
    - [How-To Geek Article](https://www.howtogeek.com/658194/windows-10s-new-update-is-deleting-peoples-files-again)
    - [The Verge Article](https://www.theverge.com/2018/10/6/17944966/microsoft-windows-10-october-2018-update-documents-deleted-issues-windows-update-paused)
    - [Windows Central Article](https://www.windowscentral.com/windows-10-october-2018-update-seems-be-deleting-users-data)

- **Security, or the lack thereof. **Millions of new Viruses and Malware EVERY MONTH**. Absolutely not worth explaining further, as everyone is aware about it.**

The problems have been amplified since the launch of Windows 10 and this situation has demanded a solution for millions in the past decade.

Till now, many have attempted to use Linux/Mac in favour of switching away from Windows, but there were few applications only available on Windows. 
Some of the most effective solutions to that include:

  - Using Linux and running Windows in a container (VM)
  - Using older versions of Windows (Not suitable today)

Running Windows in a Container is the best solution for the longer term, if the software you need isn't available on Linux/Mac. Some modifications are done following the initial install to optimize windows which will lead to better performance compared to a standard Windows computer.

## Advantages:

  - **Efficient Memory usage**: Reducing Windows background processes frees up memory for your applications.

  - **Enhanced Security**: Containerization ensures extra layers of security for the Enterprise, Universities and the Military that need it.

  - **Lower Price**: Ability to run multiple computers at potentially half the price of traditional parts.

  - **Multiple Users**: One Computer can be used by multiple simultaneous users.

![Before](https://raw.githubusercontent.com/thegamerhat/cybrdise-blog-hugo/master/content/posts/images/quickvm1.png)

![After](https://raw.githubusercontent.com/thegamerhat/cybrdise-blog-hugo/master/content/posts/images/quickvm2.png)

This Quick-VM Project aims to bring the technology of Virtualization to the masses, by not only providing a secure and faster way to use Windows, but also extending the lives of the already running computers across the globe.



## Disadvantages:

  - **Initial Setup is difficult and time consuming**

  - **Setup may vary between various devices** 

  - **Lack of customer awareness**

This Quick-VM Project aims to bring the technology of Virtualization to the masses, by not only providing a secure and faster way to use Windows, but also extending the lives of the already running computers across the globe.

# How to setup?

This Project was a long time in making, and most of the work went into automating most of the things and documenting how everything works and the necessary tweaks along with troubleshooting steps.

On an average computer, with a decent internet connection, the setup has had a total time of **100 Seconds**!

## Pre-requisites:

1. **Latest Linux based OS** (_Ubuntu/Fedora/Debian/Manjaro etc. will work great_)
2. **Internet Connection**
3. **Multiple monitors** (_Optional_)


## 🏅 Simple Install
### Step 🥇 ➜ Step 🥈 ➜ Step 🥉

### 🥇 Getting ISOs Ready

1. **Download** [Windows 10 Pro ISO](https://www.microsoft.com/en-us/software-download/windows10ISO), **and** [VirtIO Drivers (Stable)](https://fedorapeople.org/groups/virt/virtio-win/direct-downloads/stable-virtio/virtio-win.iso)

2. **Place the ISOs in** `~/WindowsVM/`

3. **Rename the ISOs as shown below:**
    - **Windows 10 ISO** ➜ `win10.iso`
    - **VirtIO Drivers** ➜ `virtio-win.iso`


### 🥈 One-liner to Setup KVM

#### Paste this in your terminal

```bash
bash <(wget -qO- https://git.io/JOeOs)
 ```

### 🥉 Getting the VM Ready:

#### Follow this [Step by Step Guide](https://github.com/thegamerhat/quick-vm/blob/main/docs/diy-vm.md#creating-a-vm)

### 🎉 That's it, You have successfully created a VM!
