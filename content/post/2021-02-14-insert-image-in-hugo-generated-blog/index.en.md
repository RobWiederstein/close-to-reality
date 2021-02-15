---
title: Insert Image in Hugo-generated Blog
author: Rob Wiederstein
date: '2021-02-14'
slug: []
categories:
  - hugo
tags: []
lastmod: '2021-02-14T16:56:20-06:00'
keywords: []
description: ''
comment: no
toc: yes
autoCollapseToc: no
postMetaInFooter: no
hiddenFromHomePage: no
contentCopyright: no
reward: no
mathjax: no
mathjaxEnableSingleDollar: no
mathjaxEnableAutoNumber: no
hideHeaderAndFooter: no
flowchartDiagrams:
  enable: no
  options: ''
sequenceDiagrams:
  enable: no
  options: ''
---


# Image 1
```md
<!--markdown-->
![another image](img/love.jpg)
```
![another image](img/love.jpg
)

# Image 2
```html
<img src="./img/love.jpg" alt = "another image">
```
<img src="./img/love.jpg" alt = "another image">

# Image 3

```html
<figure>
<img src="./img/love.jpg" alt = "another image">
<figcaption><figcaption><span>Credit:  Photo by <a href="https://unsplash.com/@solenfeyissa?utm_source=unsplash&amp;utm_medium=referral&amp;utm_content=creditCopyText">Solen Feyissa</a> on <a href="https://unsplash.com/?utm_source=unsplash&amp;utm_medium=referral&amp;utm_content=creditCopyText">Unsplash</a></span></figcaption></figcaption>
</figure>
```
<figure>
<img src="./img/love.jpg" alt = "another image">
<figcaption><span>Credit:  Photo by <a href="https://unsplash.com/@solenfeyissa?utm_source=unsplash&amp;utm_medium=referral&amp;utm_content=creditCopyText">Solen Feyissa</a> on <a href="https://unsplash.com/?utm_source=unsplash&amp;utm_medium=referral&amp;utm_content=creditCopyText">Unsplash</a></span></figcaption>
</figure>
