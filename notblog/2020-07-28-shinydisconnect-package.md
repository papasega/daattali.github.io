---
title: "{shinydisconnect}: Show a nice message when a Shiny app disconnects or errors"
tags: [professional, rstats, r-bloggers, packages, shiny]
share-img: "https://deanattali.com/img/blog/shinydisconnect/shinydisconnect.png"
permalink: /blog/shinydisconnect-package/
date: 2020-07-28 11:00:00 -0400
gh-repo: daattali/shinydisconnect
gh-badge: [follow, star]
---

Have you ever noticed how an error in your Shiny app looks very different when it happens locally (in RStudio on your laptop) compared to when it happens in production (in shinyapps.io or Shiny Server or Connect)? Locally, when a Shiny app breaks, you just get a grey screen. But when a deployed app breaks, you also get a little strip that says "Disconnected from server. Reload."

[![shiny default message]({{ site.url }}/img/blog/shinydisconnect/shinydisconnect-default-message.png){: .center }]({{ site.url }}/shinydisconnect/shinydisconnect-default-message.png)

You don't have any control over that message's text or position, and you don't have a way to get that message to appear both locally and in deployed apps.

Well, at least you didn't until now. The new {shinydisconnect} package solves exactly these two issues, by allowing you to show a customized (and pretty!) message when a Shiny app disconnects or errors, regardless of where the app is running.

You can visit the [GitHub page](https://github.com/daattali/shinydisconnect/) or check out a demo online:

<div style="text-align:center;">
<a class="btn btn-lg btn-success" href="https://daattali.com/shiny/shinydisconnect-demo/">Check out a demo</a>
</div>

# Table of contents

- [Background](#background)
- [Overview](#overview)

## Background {#background}

When I created [CRANalerts](https://cranalerts.com/) a few years ago, I wanted to make it look beautiful and not at all like a Shiny app. After investing a lot of time on making it look great, there was still one last thing I wasn't happy about: that dreadful message "Disconnected from server" message. It didn't show up when I was developing the app locally, and it wasn't really part of the shiny app - it's actually the shiny server that creates it. It was just so ugly and not user-friendly.

I searched the internet for a solution, and there was none. There were other people asking for solutions, but none offered. I couldn't just let it go, and after many anxious hours of thinking I may have to settle for something I don't like, I eventually found a way to customize it. 

[![shinydisconnect simple look]({{ site.url }}/img/blog/shinydisconnect/shinydisconnect-simple.PNG){: .center }]({{ site.url }}/shinydisconnect/shinydisconnect-simple.PNG)

For the past year, I've been often asked what my next shiny-related package is going to be. I've had a few packages in the works, but it's certainly been a while since I released a new package to CRAN! Well actually, I've created quite a few cool packages this year for clients, but none that are public and can be shared with the world unfortunately... Last week I finally got a new package to CRAN: {shinydisconnect}. It allows you to very easily 