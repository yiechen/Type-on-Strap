---
layout: post
title: Why I choose Jekyll for this website
feature-img: "assets/img/pexels/desk-nerd.jpeg"
thumbnail: "assets/img/thumbnails/desk-nerd.jpeg"
tags: [Blog]
excerpt_separator: <!--more-->
---

This is a note about my choice of using GitHub and Jekyll for this website.

When you want something simple, having a usual WordPress site often comes with a lot of other things: a web hosting plan, updating plugins, monitoring auto-updates so your site's template and functionality don't break, a MySQL database, dealing with being a target for hackers, a lot of clicking around and fussing with settings, hacking Thesis, and on and on. For a personal website that features just few pages, a CV, and maybe a place to write blog posts and link to your social media accounts and departmental web pages, WordPress is bloated. 

Do I really need to make a database call to serve an About page with less than 500 words on it? No. Do I want a bunch of third-party scripts from whatever plugin author(s) just to have social sharing tools? No. Do I want to have to hack PHP in an existing WordPress template to adjust the banner for my logo or to just simplify the user experience? No. I still want to be able to get up and running in less than five minutes, but can't it be a little lighter?

So I made a wishlist of the things I wanted for a personal website:

* simplicity
* good performance and reliability
* no databases
* hosting to be free or really cheap
* the ability to work on my site from anywhere if needed
* to use open source tools supported by an active development community
* to get up and running quickly
* to be able to share my code so others can easily re-use it

There are a lot of lightweight CMS options out there, but I fell for the GitHub + Jekyll toolchain. It's well known and now pretty established, and the partnership it has developed with Jekyll developers (it's based in Ruby) and its use of Markdown to separate content from markup just seemed to click with me.

That's why after building my site with the help of many sources, I've finally taken it a step further and replicated the best <a href="/_includes/guide_github-pages.html" title="Creating and Hosting a Personal Site on GitHub">beginner's guide to getting started building and hosting a personal website and blog with GitHub Pages and Jekyll</a>. It is very step-by-step. It even refactors code to teach you how Jekyll templates work.
