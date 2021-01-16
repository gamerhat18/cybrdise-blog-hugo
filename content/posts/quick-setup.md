---
title: "Quick Setup"
date: 2021-01-16T12:02:16+05:30
author: "Pranav Kulkarni"
authorTwitter: "gamerhat18" #do not include @
cover: ""
tags: ["RemoteDesktop", "ASAP"]
keywords: ["TeamViewer", "Setup"]
description: "A Simple way for everyone to setup a new remote PC from scratch,  regardless of the Operating system."
showFullContent: false
draft: false
---


Here are some one-liners for quick and easy first setups of various operating systems.
Check out this to learn more: [Quick-Setup](https://github.com/gamerhat18/quick-setup)


## Linux (without sudo):

```bash
curl -sSL https://git.io/JLxkS | bash
```

>Here are the things that it does on Linux:
>
>1. Updates repositories via `sudo apt update`.
>2. Downloads and Installs TeamViewer from the official website.
>3. Installs ZSH and Oh-My-ZSH.
>4. Replaces .zshrc & .bashrc with my personal rc files.
>5. Opens TeamViewer and I ask the client to send a picture of the id and password.
>6. Gets other scripts for more personalized configurations.

## Windows (Administrator Privileges needed):

```powershell
iex ((New-Object System.Net.WebClient).DownloadString('https://git.io/JtUwY'))
```

>Here are the things that it does on Windows:
>
>1. Installs Chocolatey.
>2. Installs TeamViewer from Chocolatey.
>3. Installs QBittorent from Chocolatey for downloading Linux ISO(s).
>4. Downloads Rufus for writing the ISO to a USB Stick.
>5. Opens TeamViewer and I ask the client to send a picture of the id and password.
>6. Gets other scripts for more personalized configurations.
