+++ 
draft = false
date = 2021-06-09T13:16:52-04:00
title = "Start"
description = ""
slug = ""
authors = ['Brian Knight']
tags = ['meta']
categories = ['meta']
externalLink = ""
series = []
+++

Twenty-five years after first considering it, I have finally launched a a personal website. In the interim, I gained enough life experience and perspective to feel confident about publishing something of interest to readers.

## Some for Me, Some for You
I am a software engineer by day. This site will not be about technical matters, however. There is plenty of technical content out there in the world and, frankly, I have long since tired of the business of technology. Candidly, I am one of the best cloud engineers in the biz, but I no longer take much pride or identity from my work in that sphere. I gave my heart at the office and it was a mistake.

Instead, this site is a project focused on finding my voice again. I make no promises about what kind of content will be found here in the future. I am simply following my nose. My interests are wide and varied - I take a butterfly-net approach to learning. I hope you will find the content here interesting, thought-provoking, and well-written. I am committed to this process and welcome all feedback. 

## Under the Hood
This site is generated as static HTML using the [Hugo](https://gohugo.io) framework. I want to use a static site generator other than [Jekyll](https://jekyllrb.com), and Hugo appeals to me because it is simple and written in Go.

I picked the [Coder](https://themes.gohugo.io/hugo-coder-portfolio/) theme for its clean and simple approach and its support for Dark mode. Two days after I started working on the site, I happened upon a link to [a blog post](https://www.engjole.net/posts/wow-how-many-times-can-i-say-smarandache-wellin-number/) written by the wonderful [Enny Jole](https://www.engjole.net) and discovered that they are using the exact same framework and theme for their site. I hope I can be forgiven for this collision of tastes.

Being an engineer, I indulged myself with the hosting of the site. The configuration and content reside [on GitHub](https://github.com/brianknight10/mostlyinvisible). When I push new changes to the repository, [a GitHub Action](https://github.com/features/actions) generates a new version of the site and pushes the files to a [Cloud Storage](https://cloud.google.com/storage) bucket in [Google Cloud](https://cloud.google.com).  The files are fronted by a load balancer and a content-delivery network to improve performance and reliability. It’s a simple and elegant setup that provides the flexibility for whatever I choose to do here.