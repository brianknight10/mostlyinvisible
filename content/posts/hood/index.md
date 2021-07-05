+++ 
draft = false
date = 2021-07-02T13:16:52-04:00
title = "Under the Hood"
description = ""
slug = ""
authors = ['Brian Knight']
tags = ['meta', 'technical']
categories = ['meta']
externalLink = ""
series = []
+++

From hikers to bikers, sailors to soldiers, discussions among practitioners often end up revolving around gear. I have noticed that bloggers and website owners follow the same practice. Accordingly, I describe my site setup and publishing process in layperson's terms for the curious.

At the start, I laid out the following design requirements:
- No management of servers or databases required
- Support for writing in [Markdown](https://www.markdownguide.org)
- An automated publishing workflow
- Easy scalability and hands-off fault tolerance

These requirements will serve my modest ambitions for the amount of traffic expected on this site, combined with my desire to focus on the content. 

Early on, I decided to serve this site as static HTML code. When you visit this page in your browser, there is no server waiting to generate the page contents dynamically. Instead, this page was created as a file when I published it. Your request results in the server just returning the file. No database is necessary, and the site is lightning fast.

Writing raw HTML is cumbersome and time-consuming. Enter the [Hugo](https://gohugo.io) framework. Hugo provides a way for me to write my content in Markdown and then translates it into HTML when I publish the site. There are many other static site generators, but Hugo appealed to my desire for simplicity and speed.

I am a poor web designer. I don't know how to make websites look right on mobile devices and desktop screens. I can't choose colors or fonts well. No matter, as Hugo community members offer [hundreds of themes](https://themes.gohugo.io) that I can select for free. I picked the [Coder](https://themes.gohugo.io/hugo-coder-portfolio/) theme for its clean and straightforward approach and its support for Dark mode.[^1]

I store all of my content and configuration in [GitHub](https://github.com/brianknight10/mostlyinvisible). Whenever I create new content or a change, I push the files from my computer into the repository. The push [fires an action](https://github.com/features/actions) in GitHub that starts the publishing process.

Using a couple of short Hugo commands, the publishing process translates the site into static HTML files and uploads them to a [Cloud Storage](https://cloud.google.com/storage) bucket in [Google Cloud](https://cloud.google.com). You can think of Cloud Storage as a remote disk drive - similar to [Google Drive](https://drive.google.com). However, I have configured Google Cloud to go one step further. Google can store copies of the static files worldwide in a [content-delivery network](https://en.wikipedia.org/wiki/Content_delivery_network) or CDN. If you access this site from Tokyo, you will most likely receive the files from a Japanese storage location. If you are in New York City, the files probably will be delivered from somewhere in New York.

Leveraging Hugo and Google Cloud gives me the freedom to create content without fussing with the underlying technology. The site is extremely cheap to operate, fault-tolerant, and can support any number of visitors.

Any questions? Please [send an email](mailto:brianknight@hey.com).

[^1]: Two days after I started working on the site, I happened upon a link to [a blog post](https://www.engjole.net/posts/wow-how-many-times-can-i-say-smarandache-wellin-number/) written by the brilliant [Enny Jole](https://www.engjole.net) and discovered that they are using the same framework and theme for their site. I hope they can forgive me for this collision of tastes.