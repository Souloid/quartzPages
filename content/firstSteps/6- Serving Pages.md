---
title: 6- Serving Pages
draft: false
tags: 
created: 2024-07-08 @ 00:47:44 AM
updated: 2024-07-08 @ 05:00:30 AM
---
 
Upon syncing to github I noticed that my time properties are displayed in github

# Running the local server to serve and test our pages

In order to test what things would look like without publishing them, let's run a local server on our machine to push pages to it and test how it all looks. 

Follow the instructions from this [page](https://quartz.jzhao.xyz/build) and run the following commands:

```
npx quartz sync
npx quartz build --serve
```

In a browser of your choice (doesn't have to be inside WSL) go to `localhost:8080` 

How's it all look? This is your current website as Quartz built it for you. Explore those pages and see what happens. Modify them in obsidian and see the changes happen. 

When you're done messing around you can make webpages under content using the template or using longform which uses the template. 

I don't feel like explaining this to you in boring detail because I don't want to put a damper on your excitement. If you actually get stuck or confused check out the "Scenes" tab under the longform tab.

If that's too hard, just go to the content folder, create a new note, and then inside that note open the command palette of obsidian by typing `ctrl + P` and then start by typing template, click the option "Insert Template". 
This will use your template to modify that new note into the proper syntax for Quartz' webpages. 



With this we're creating pages :D 
Congrats now you're an artist :3

Let's go figure out how to host these pages online using our github repo.
