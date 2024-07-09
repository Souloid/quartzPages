---
title: 4- Installing Obsidian
draft: false
tags: 
created: 2024-07-08 @ 00:47:44 AM
updated: 2024-07-08 @ 23:26:22 PM
---

I tried to open the files for this project using my local obsidian app (on windows) but it couldn't connect to the networked WSL so I had to open firefox to install obsidian locally in WSL and try to use that.

Here's what I did:
1. installed firefox with by typing into my WSL terminal the command `sudo apt install firefox`
2. opened it by typing into my terminal `firefox`
3. searched for obsidian's website and opened it, downloaded the debian installer cause my WSL instance is an ubuntu which is debian based.
4. I navigated to home/snap/firefox/common/Downloads/ to find the downloaded obsidian installer
5. I tried to install it but I got this error:
```
wslUserName@pcMachine:~/snap/firefox/common/Downloads$ sudo dpkg -i obsidian-1.6.5-amd64.deb
[sudo] password for wslUserName:
Selecting previously unselected package obsidian.
(Reading database ... 51106 files and directories currently installed.)
Preparing to unpack obsidian-1.6.5-amd64.deb ...
Unpacking obsidian (1.6.5) ...
dpkg: dependency problems prevent configuration of obsidian:
 obsidian depends on libgtk-3-0; however:
  Package libgtk-3-0 is not installed.
 obsidian depends on libnotify4; however:
  Package libnotify4 is not installed.
 obsidian depends on libnss3; however:
  Package libnss3 is not installed.
 obsidian depends on libxtst6; however:
  Package libxtst6 is not installed.
 obsidian depends on xdg-utils; however:
  Package xdg-utils is not installed.
 obsidian depends on libatspi2.0-0; however:
  Package libatspi2.0-0 is not installed.
 obsidian depends on libsecret-1-0; however:
  Package libsecret-1-0 is not installed.

dpkg: error processing package obsidian (--install):
 dependency problems - leaving unconfigured
Processing triggers for hicolor-icon-theme (0.17-2) ...
Errors were encountered while processing:
 obsidian
wslUserName@pcMachine:~/snap/firefox/common/Downloads$
```

That means we need to install some pre-requisites to be able to install obsidian.

Let's do just that. Run the command:
```
sudo apt install libgtk-3-0 libnotify4 libnss3 libxtst6 xdg-utils libatspi2.0-0 libsecret-1-0
```
Ran into issues that were fixed with `sudo apt --fix-broken install -y`

We're finally there. Open the WSL instance of obsidian by typing `obsidian`

See you in the [[5- Configuring Obsidian|next page]] :3
