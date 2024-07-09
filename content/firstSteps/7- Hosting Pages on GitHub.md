---
title: 7- Hosting Pages on GitHub
draft: false
tags: 
created: 2024-07-08 @ 00:47:44 AM
updated: 2024-07-08 @ 23:27:49 PM
---
 
# Configuring Quartz
As per the website [hosting](https://quartz.jzhao.xyz/hosting) instructions: using vscode we're going to create a new file under (yourQuartzRootFolder)/.github/workflows named deploy.yml

Paste the configuration listed on their website as follows:
```
name: Deploy Quartz site to GitHub Pages
 
on:
  push:
    branches:
      - v4
 
permissions:
  contents: read
  pages: write
  id-token: write
 
concurrency:
  group: "pages"
  cancel-in-progress: false
 
jobs:
  build:
    runs-on: ubuntu-22.04
    steps:
      - uses: actions/checkout@v4
        with:
          fetch-depth: 0 # Fetch all history for git info
      - uses: actions/setup-node@v4
      - name: Install Dependencies
        run: npm ci
      - name: Build Quartz
        run: npx quartz build
      - name: Upload artifact
        uses: actions/upload-pages-artifact@v3
        with:
          path: public
 
  deploy:
    needs: build
    environment:
      name: github-pages
      url: ${{ steps.deployment.outputs.page_url }}
    runs-on: ubuntu-latest
    steps:
      - name: Deploy to GitHub Pages
        id: deployment
        uses: actions/deploy-pages@v4
```

On github's website, go to your repo, settings, pages, source, select github actions. 
Then in your wsl terminal run the command `npx quartz sync`.
This will push the updates to your github page and actually host the page :D

Check it out! Go with your favorite browser to the link `githubUsername.github.io/repoName` replacing those obvious placeholders with your own github user name and repo name :3

CONGRATS!!!!~~~~

I'm gonna go buy(rent) myself a domain name (aka website address) so I can [[8- Setting Up a Custom Address|make it look fancy in the address bar]]. I don't wanna see github.io and stuff out there D:
