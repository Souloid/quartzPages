---
title: Setting the stage
draft: false
tags: []
created: 2024-07-08 @ 00:47:44 AM
updated: 2024-07-08 @ 02:39:57 AM
---
So I wanted a safe sandbox for me to play with, since I unfortunately use windows I decided to play with a WSL ubuntu instance so that I can just wipe it all out if it breaks. 

BTW~ WSL on windows is PERFECT as a sandbox to try out software installations and deployments cause you can just wipe the sucker and restart. Don't you just love VMs?

So I spun up a good ol' Ubuntu-22.04 WSL2 instance and updated everything with sudo apt update and upgrade.

Oh right I'm supposed to show you how.... 

uhh.... lookup how to setup a WSL instance on youtube <.<

In a nutshell:
1. Enable virtualization in your bios (depends on your pc motherboard)
2. Enable WSL in windows features (seriously just look it up it takes 10 seconds)
3. Open up windows powershell and type the following
```
wsl --install Ubuntu-22.04
```
4. Makeup a username for your new linux VM
5. Makeup a password and remember it
6. Now that you're in (you'll know it when you see the cursor's last line ending with $) type the following commands to update your VM
```
sudo apt update && sudo apt upgrade -y
```
update will get you the latest list of updates for your linux kernel, and upgrade will install them. the "-y" parameter will answer "yes" for you when it asks if you want to download the files.
7. Type in your password that you definitely remember
8. AND our sandbox is ready~ congrats 