---
title: 2- Installing the Quartz Project
draft: false
tags: 
created: 2024-07-08 @ 00:47:44 AM
updated: 2024-07-08 @ 23:25:32 PM
---

In your WSL (or linux) let's make sure you're in the home directory just so we're all on the same starting point.

Type the following command to make sure we're in the home directory:
```
cd ~
```

Now we will install [Quartz](https://quartz.jzhao.xyz/) cause that will be where we make our website. Following the instructions from their website [here](https://quartz.jzhao.xyz/).

I wanna make a folder so can I keep things organized.
In your terminal type:
```
mkdir yourFolderName
cd yourFolderName
```

The instructions specify that we need to have NodeJS and NPM (node package manager ) installed as well. So I went to Node's [website](https://nodejs.org/en/download/package-manager) and found the installation instructions for linux.
In your terminal type:
```
# installs nvm (Node Version Manager)
curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.39.7/install.sh | bash

# download and install Node.js (you may need to restart the terminal)
nvm install 20

# verifies the right Node.js version is in the environment
node -v # should print `v20.15.0`

# verifies the right NPM version is in the environment
npm -v # should print `10.7.0`
```

Now let's get on with those [instructions](https://quartz.jzhao.xyz/#-get-started):
```
git clone https://github.com/jackyzha0/quartz.git
cd quartz
npm i
npx quartz create
```
When I ran `npm i` I ran into 3 vulnerabilities that I fixed with `npm audit fix`

This is where I might change things in the future. Setting up I chose "treat links as shortest path" which is made to resemble obsidian, rather than "absolute path" which matches HUGO. If I use HUGO for generating my next website (resume/online portfolio) I would chose absolute path. But since this website is for sharing notes and writing lengthy guides we're gonna go with shortest path this time :3
```
  Quartz v4.2.3
│
◇  Choose how to initialize the content in `/home/yourNotSoSecretUsername/yourFolderName/quartz/content`
│  Empty Quartz
│
◇  Choose how Quartz should resolve links in your content. This should match Obsidian's link format. You can change this later in `quartz.config.ts`.
│  Treat links as shortest path
│
└  You're all set! Not sure what to do next? Try:
  • Customizing Quartz a bit more by editing `quartz.config.ts`
  • Running `npx quartz build --serve` to preview your Quartz locally
  • Hosting your Quartz online (see: https://quartz.jzhao.xyz/hosting)
```

See you in the next page ([[3- Setting up our GitHub Repo|setting up our github repo]]) :)


