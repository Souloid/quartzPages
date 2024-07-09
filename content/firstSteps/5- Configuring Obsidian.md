---
title: 5- Configuring Obsidian
draft: false
tags: 
created: 2024-07-08 @ 00:47:44 AM
updated: 2024-07-08 @ 23:26:51 PM
---
# Intro to quartz in obsidian

Click on open vault, and navigate to the folder where you downloaded Quartz and select that folder.

Okay, now that we're here, we can finally view our files in obsidian and make our pages like I am doing right now. 


> [!NOTE] DONE!!!
> Now that you're here. This is all that's mandatory. You can start writing in your Contents folder the webpages that you want to see (provided that you follow the syntax explained in quartz documentation [website](https://quartz.jzhao.xyz/authoring-content))


You can technically start designing your website by going to the contents folder to start making your pages. But I'm going to install some obsidian plugins cause I like tinkering and so should you.

In obsidian, go to settings, community plugins, enable community plugins, and search for some handy dandy useful plugins. 

# Plugins
The plugins I installed can be categorized into three:
## Useful (should grab these)
1. [Templater](https://github.com/SilentVoid13/Templater) This will help me program the syntax so I don't have to manually do it for each page.
2. [Paste URL into Selection](https://github.com/denolehov/obsidian-url-into-selection) This helps me quickly put links into the words like [this](https://github.com/denolehov/obsidian-url-into-selection).
3. [Note Refactor](https://github.com/lynchjames/note-refactor-obsidian) This is in case I want to extract a wall of text into its own note (page?) using the command palette of obsidian (you really should explore videos online about these plugins they're so cool)
## Cool (optional)
1. [Update Time on Edit](https://github.com/beaussan/update-time-on-edit-obsidian) (I like seeing time stamps ok?)
## Tasteful (experimental)
1. [Longform](https://github.com/kevboh/longform) (helps writers apparently so I'll use it to format my notes like book chapters :3)


# Configuring Plugins

## [Templater](https://github.com/SilentVoid13/Templater)
I created a folder and named it "Assets" to organize my files and notes.
In it I created another folder to host my templates.
I will use a template that contains the proper syntax for for publishing Quartz webpages.

Then I created a template within the templates folder and added the syntax from the quartz [website](https://quartz.jzhao.xyz/authoring-content) to it.

```
---
title: Example Title
draft: false
tags:
  - example-tag
---
 
The rest of your content lives here. You can use **Markdown** here :)
```

## [Update Time on Edit](https://github.com/beaussan/update-time-on-edit-obsidian)
I changed the format of the date a bit and then I clicked update all files. This will add two properties to all my files, one has the date of creation and one has the date of modification. Helps me remember when something was added and when it was last changed. 

> [!Warning] Unnecessary and Will Show up on GitHub
> This is just for me to keep track of things that break my stuff. I want to know if something broke due to a file being added, or if it broke due to a file being changed.

## [Longform](https://github.com/kevboh/longform)
This is my first time using this. For now I started by naming this project first steps. Then I set it to use the template I created under the templates folder. 

I think this is good enough for Obsidian. Let's move on to shipping those pages off.

See in the [[6- Serving Pages|next page]] :)