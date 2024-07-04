---
title: "Creating a Blog with Hugo and Obsidian"
date: 2024-07-03T22:53:58+05:30
draft: false
author: "Erik A"
tags:
  - Hugo
  - Obsidian
  - DigitalOcean
image: /images/obsidian-hugo-blog.jpg
description: "An introductory post"
toc: 
---
Creating a blog with static websites is very easy. 

This is particularly easy if you are familiar with markdown and use tools like [Obsidian](obsidian.md). All you need to do is leverage a tool like [DigitalOcean](www.digitalocean.com) to deploy a [Hugo](www.gohugo.io) template.

With this template, a foundation for a blog is available for you to modify yourself.

Let's do it!

> Required Tools: [Git](https://www.git-scm.com/downloads), [hugo cli](https://gohugo.io/installation/)

## Getting up to Speed with Hugo
1. Find a [theme](https://themes.gohugo.io/).
2. `hugo new site <name-of-site>`
3. `cd <name-of-site>`
4. `git submodule add --depth=1 https://github.com/{GITHUB_THEME_USER}/{GITHUB_THEME}.git themes/{GITHUB_THEME}`
	1. Example: `git submodule add --depth=1 https://github.com/adityatelange/hugo-PaperMod.git themes/PaperMod`
5. Ensure that you have updated the parameters of your `config.toml`
	1. `theme = PaperMod`
6. Run the app
	1. `hugo server`

## Push to Git
```bash
# Create a new repository on the command line
touch README.md
git init
git add README.md
git commit -m "init commit"
git remote add origin https://github.com/{user}/{repository}.git
git push -u origin main
 
# Push an existing repository from the command line
git remote add origin https://github.com/{user}/{repository}.git
git push -u origin main
```

## Add A Post
1. Run the command: `hugo new post/<name-of-post>.md`
2. Open in [Obsidian](https://obsidian.md/) 
3. Write your post!
4. Push to Git

## Leverage DigitalOcean to Deploy
1. Create or sign into a [DigitalOcean](https://digitalocean.com) account
2. Navigate to Manage ➡️ Apps ➡️ Create App
3. Select your Github Provider
4. Select the repository
5. DigitalOcean will automatically recognize the app is a Hugo app
6. Select Next ➡️ Skip to Review
7. Ensure the Routes value is `/`
8. Select Create Resources
9. The app will now deploy to a DigitalOcean Url

## Conclusion
With that, we can have an easy, markdown-driven blog that is completely free. 