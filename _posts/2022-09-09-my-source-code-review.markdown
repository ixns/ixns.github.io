---
layout: post
title:  "Choosing a stack: how I review code"
date:   2022-09-09 05:08:52 -0500
categories: coding code shopify 
---
# Choosing a stack: how I review code
Recently I've been learning more about the Shopify API, and building out my own minor Shopify app prototypes. Due to the opiniated nature of creating Shopify apps (you must use their UI library, follow *their* authentication flow, look for *their* cookies, etc) , I've had the need to browse through other Shopify app source codes in order to understand how everything pieces together.

In doing this, it was initially difficult to review the code effectively. To begin, I pulled up some of the source codes into VSCode, using the tree browser to pick through the folders and inspect the files one by one. This works for the most part. VSCode has built in function-click-through which makes understanding each of the functions pretty easy.

That's great, but for the most part looking at the actual functions being called is a distraction from the logical flow of the code.

When I read books, I skim through them generally. Writers tend to add plenty of fluff. by skipping sections you deem unimportant, you can find the core message of a text (with some margin of error) and then build upon it by reading often, preferably in many different frames of mind so as to extract the most meaning from it.

When it came to using VSCode to review Shopify app source codes, I applied this very Principle of Skimming, but got annoyed very quickly that I had to click on the next source file in order to open it, every time.

## My source code review workflow
So after getting annoyed and frustrated with VSCode, I booted up my terminal. And in doing this, I came up with a pretty great system for reviewing source codes in a productive and non-distracting way:

1. Go to the root folder of the source code
2. ``cd`` continuously until you find a folder which has a good amount of source files, all of which share the same extension (in my case it was .ts)
3. type ``vim *.{file extension}``
4. skim through whatever source file comes first (press 5 and then k repeatedly to move fast). find the main purpose of the file, as if you were reading a page from a book. ignore the small details if they don't help you to evaluate its purpose.
5. after you have a vague idea what the file does, type the command ``:n`` in vim
6. rinse and repeat until you've read all the files in that folder, then proceed onto other folders


Using this method is great because it requires very little. Furthermore, if you bring vim into fullscreen while doing this, it becomes immersive and distractionless. It lets you focus on just reading source files. And working in the terminal is always some fun.

<span style="color:blue">ixns</span>.

![Wealth is of the heart and mind, not of the pocket](https://m.media-amazon.com/images/I/51zRy3g-4XL.jpg)
