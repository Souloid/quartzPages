---
title: Setting up our GitHub Repo
draft: false
tags: []
created: 2024-07-08 @ 00:47:44 AM
updated: 2024-07-08 @ 03:42:39 AM
---
 
Go to https://github.com/ and register. Make a new Repository and follow the instructions from this [Quartz Page](https://quartz.jzhao.xyz/setting-up-your-GitHub-repository). 

1. Make new Repo
2. Give it a nice name like my-Totally-Awesome-Website-That-I-Will-Definitely-Use-More-Than-Once 
3. Set it to public cause people wanna see it. By people I meant your future stalkers. You popular you~
4. DO NOT initialize with a read me or gitignore 
5. License.... idk~ I'm not a lawyer so I'll let you take responsibility for that one but we can start with "no license"
6. Click "Create repository" .... repository suppository.... you cannot unsee that 

Now that you have a repo to hold our website we're gonna configure our WSL to send stuff to it.

Copy the repo link which should look like: `https://github.com/yourGitHubUserName/yourRepoName.git`

In your WSL (linux) terminal type the following:
```
# list all the repositories that are tracked
git remote -v
 
# if the origin doesn't match your own repository, set your repository as the origin
git remote set-url origin thatLinkYouJustCopied
 
# if you don't have upstream as a remote, add it so updates work
git remote add upstream https://github.com/jackyzha0/quartz.git
```

Now just to check we're good type:
```
git remote -v

# you should get something that looks like this

linuxUserName@pcName:~/yourFolderName/quartz$ git remote -v
origin  https://github.com/yourGitHubUserName/yourRepoName.git (fetch)
origin  https://github.com/yourGitHubUserName/yourRepoName.git (push)
upstream        https://github.com/jackyzha0/quartz.git (fetch)
upstream        https://github.com/jackyzha0/quartz.git (push)>)
```

OK~ time to send our files to that repo now:

```
npx quartz sync --no-pull
```

I ran into an issue: I'm telling my linux machine to send files to my repo.... but I didn't tell it who I am.... so now my github repo refused the connection cause it doesn't know who's sending it. Let's fix that

```
*** Please tell me who you are.

Run

  git config --global user.email "you@example.com"
  git config --global user.name "Your Name"

to set your account's default identity.
Omit --global to set the identity only in this repository.
```

This is where some of you guys who are linux ninjas might do it your own way.

Remember how I'm using a windows machine with WSL? yeah this is my journey so writing about MY experience.

 had to verify my github login info. I decided to proceed within vs code. So I typed (this is only for WSL) `code .`

Install WSL extension so that you can use vscode to manipulate files and use its terminal in your WSL VM. (you should get popups that will guide you)

Used vscode to login to my GitHub with its extension (again it was just a popup for me when I ran that sync command from before). Then I opened a terminal in vscode to continue typing commands into my WSL. 

I wanted to use this name and email for this repo only so I removed --global from the suggested command.
```
git config user.email "you@example.com"
git config user.name "Your Name"
```

OK ONE LAST TIME LETS TRY IT!
```
npx quartz sync --no-pull
```

AND~ it's DONE!!! it worked! it sent it to my repo and the files in the repo on github changed!

You hungry? I'm hungry... let's take a break and I'll see you in the next page (Installing Obsidian)

