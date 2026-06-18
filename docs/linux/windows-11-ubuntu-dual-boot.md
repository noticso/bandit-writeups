# How I Set Up a Windows 11 and Ubuntu Dual Boot System

## Overview

As part of my cybersecurity and programming learning journey, I decided to set up a dual boot system with Windows 11 and Ubuntu LTS.

My goal was to keep Windows available for everyday use while having a dedicated Linux environment for learning command-line tools, programming, cybersecurity fundamentals, networking, and future hands-on labs.

I allocated **200 GB** of disk space to Ubuntu, giving me enough room to install development tools, security utilities, virtual machines, and future projects.

## Why I Chose Dual Boot

I considered using virtual machines, but I wanted to experience Linux directly on my computer as well.

A dual boot setup allows me to choose between Windows 11 and Ubuntu every time I start the computer. This gives Ubuntu direct access to the hardware and provides a more complete Linux learning experience.

For my current goals, dual boot is useful because I want to learn:

* Linux command-line basics
* Cybersecurity tools and workflows
* Programming and scripting
* Networking concepts
* System configuration
* File permissions and user management
* Virtualization and homelab environments

## Creating the Ubuntu Installation USB

I downloaded the Ubuntu LTS installation image and used **balenaEtcher** to create a bootable USB drive.

Rather than copying the Ubuntu ISO file manually to the USB drive, balenaEtcher writes the image correctly and turns the USB drive into an installation device.

This was especially useful because the Ubuntu ISO was larger than the normal FAT32 single-file limit.

## BIOS Changes

Before starting the installation, I entered the BIOS/UEFI settings.

I made two important changes:

1. I disabled **Secure Boot**.
2. I configured the boot order so that the USB drive containing Ubuntu could be selected during startup.

This allowed my computer to boot from the Ubuntu installation USB instead of starting Windows automatically.

## Installing Ubuntu Alongside Windows 11

After booting from the USB drive, I started the Ubuntu installation process.

At one point, I accidentally selected an option different from **Try or Install Ubuntu**. Because of that, I had to restart the computer and begin the process again.

After restarting, I selected the correct installation option and continued normally.

When Ubuntu asked how I wanted to install it, I selected:

```text
Install Ubuntu alongside Windows Boot Manager
```

This was the safest and simplest choice because I wanted to keep Windows 11 installed and avoid manually creating Linux partitions.

Ubuntu then used the space I had allocated for Linux and installed itself alongside Windows.

## Final Result

After the installation was complete, the computer restarted successfully.

I can now boot into both operating systems:

```text
Windows 11
Ubuntu LTS
```

Everything is working correctly, and the dual boot setup is ready for my next steps in cybersecurity and programming.

## What I Learned

This project helped me understand several important concepts:

* The difference between a virtual machine and a dual boot system
* How bootable USB drives work
* How BIOS/UEFI settings affect operating system installation
* The role of Secure Boot during Linux installation
* How to install Ubuntu without replacing Windows
* Why it is important to read each installation option carefully

## Advice for Beginners

If you are setting up a Windows and Ubuntu dual boot system for the first time, take your time and read every screen carefully.

The most important things are:

* Make a backup of important files before changing partitions or boot settings.
* Use a reliable tool such as balenaEtcher to create the installation USB.
* Make sure you select the correct boot device in the BIOS or boot menu.
* Choose **Install Ubuntu alongside Windows Boot Manager** if you want to keep Windows.
* Do not rush through the Ubuntu startup screen, because selecting the wrong option can force you to restart the process.

## Next Steps

Now that Ubuntu is installed and working, my next goals are to:

* Learn essential Linux commands
* Practice file permissions and user management
* Install programming tools
* Build a cybersecurity homelab
* Use virtual machines for authorized security labs
* Continue learning through OverTheWire, TryHackMe, and other legal training platforms
