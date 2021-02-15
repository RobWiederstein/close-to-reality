---
title: Insert Image in Hugo Blog
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

Hugo resolved the debate over whether to group images together or to group them with the narrative of the post.  This debate was always one that I resolved with putting images along side the posts. Many times, a post is a collection of screenshots to illustrate the post's theses.  The debate was alive and well over at `jekyll` too and there was a plug-in available.  With version .36, `hugo`officially defaults to creating a folder for each blog post.  The `hugo` documentation describes "page-relative images" and how they are packaged into "Page Bundles".
With this change, you can then place you images along side the post.  The organization of my posts then is like this `https://example.com/content/post/post_title/img/image_01.jpg`.

Images can be included in a markdown document via plain markdown or wrapped in `html` tags.  Here's some examples.

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
<figcaption><span>Credit:  Photo by <a href="https://unsplash.com/@solenfeyissa?utm_source=unsplash&amp;utm_medium=referral&amp;utm_content=creditCopyText">Solen Feyissa</a> on <a href="https://unsplash.com/?utm_source=unsplash&amp;utm_medium=referral&amp;utm_content=creditCopyText">Unsplash</a></span></figcaption>
</figure>
```
<figure>
<img src="./img/love.jpg" alt = "another image">
<figcaption><span>Credit:  Photo by <a href="https://unsplash.com/@solenfeyissa?utm_source=unsplash&amp;utm_medium=referral&amp;utm_content=creditCopyText">Solen Feyissa</a> on <a href="https://unsplash.com/?utm_source=unsplash&amp;utm_medium=referral&amp;utm_content=creditCopyText">Unsplash</a></span></figcaption>
</figure>
