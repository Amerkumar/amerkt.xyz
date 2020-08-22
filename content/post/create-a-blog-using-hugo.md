---
title: "How to create a blog using hugo"
date: 2020-08-22T01:49:53+05:00
draft: false
tags: ["hugo","blog","DIY"]
---

I have recently created my first site using hugo, so I thought the first post should be the process of creating a site using hugo. 

## Step 1 - Install Hugo

Go to [Hugo releases](https://github.com/spf13/hugo/releases) and download the appropriate version for your OS and architecture. 

_**Instructions here will be relevant for windows but can be applied to other OS with some tweaks.**_

Put the hugo executable into the PATH environment variable so it accessible from everywhere. Here is the link to put hugo binary in environment variable path. [Add to the Path - Windows 10](https://www.architectryan.com/2018/03/17/add-to-the-path-on-windows-10/)

## Step 2 - Create Site Directory

Although, You can create a site from scratch using hugo, I would recommend to use themes. After going through the step one, you have to create a site directory which contains your blog configs, layouts and content. 

Go to your preferred directory i-e C,D, Documents, Desktop etc.

Open the command prompt there.

First run this command. 

```
D:\>hugo version
```

If it prints a output like below with some version number, it means hugo is correctly configured in your environment otherwise you have to repeat step 1.

```
Hugo Static Site Generator v0.74.3-DA0437B4 windows/amd64 BuildDate: 2020-07-23T16:23:30Z
```
Now run this command, it will configure with the barebones layout, content and configs to get you started. 

```
D:\>hugo new site myblog.com
```

Navigate to myblog.com using the change directory command.

```
D:\>cd myblog.com
```

## Step 3 - Install a theme

Now you can use these configs to customize your blog, but its better you should start with a theme. 

You have to install the relevant theme available on hugo platform. Here is the link to explore hugo themes. [Hugo Themes](https://themes.gohugo.io/)

For this site, I have used cupper theme. [Cupper Theme](https://github.com/zwbetz-gh/cupper-hugo-theme)

_**Please note that commands below are relevant for downloading the cupper theme,the installation process is different which is available on their relevant github page.**_

For cupper theme, here are the commands which will download cupper theme. 

```
D:\myblog.com>git init
D:\myblog.com>git submodule add https://github.com/zwbetz-gh/cupper-hugo-theme.git themes/cupper-hugo-theme
D:\myblog.com>git submodule update --remote --merge
```

## Step 4 - Run Example site

Now you will find your theme inside the themes directory, and most of the themes contains example site so first we are going to run it. 

```
D:\myblog.com\themes\cupper-hugo-theme\exampleSite>hugo server --themesDir ../..
```

The commands is also available cupper theme github page.

This will run the example site. Now you can copy relevant files from cupper-theme folder to your blog main directory.

## Step 5 - Customize your blog

If you are able to access example site successfully, then you can copy the config file and replace it with your main config file and run the hugo server again. 

_**-D option will run in draft mode which will also include the content in draft**_

```
D:\myblog.com>hugo server -D
```

Copying the config file from exampleSite folder will run your main site as it contains main config and header content required for a site. 

Now you have to modify the configs and copy the relevant content files from themes folder to your main blog folder to fix broken links. 



