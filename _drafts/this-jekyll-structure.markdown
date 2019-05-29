---
layout: post
title: This Jekyll Folder and File Structure
feature-img: "assets/img/pexels/desk-nerd.jpeg"
thumbnail: "assets/img/thumbnails/desk-nerd.jpeg"
tags: [Blog, Code, Tips]
excerpt_separator: <!--more-->
---

This is a note about my choice of folder and file structure for this website.
<!--more-->



## Structure

Here are the main files of the template

```bash
jekyll-theme-basically-basic
├── _draft	               	# To store your drafts, they won't be published on your site
├── _includes	            # theme includes (footer, header, navbar, others)
├── _layouts                # theme layouts (see reference guide for details)
├── _portfolio	            # collection of travel articles to be populated in the "portfolio" page
├── _posts                  # Blog posts
├── _sass                   # Sass partials 
├── assets
|  ├── js	               		# theme javascript, Katex, jquery, bootstrap, jekyll search, 
|  ├── css                     	# isolated Bootstrap, font-awesome, katex and main css
|  ├── fonts		       		# Font-Awesome, Glyphicon, and other fonts
|  └── img		       			# Images used for the template
|  	  ├── guides			# images exclusively used for the guide to Jekyll page
|  	  ├── pexels			# raw images from pexels
|  	  ├── portfolio   		# previews for the portfolio page (travel plans gallery)
|  	  ├── sketchplanation   # raws from sketchplanation
|  	  ├── featured          # featured images for posts from template
|     └── thumbnails		# featured thumbnails for posts on main pages
├── pages
|   ├── 404.md		       		# To be displayed when url is wrong
|   ├── about.md               	# About example page
|   ├── gallery.md              # Gallery page for your photos
|   ├── portfolio.md	        # Portfolio page for your projects
|   ├── search.html	       		# Search page
|   └── search.json            	# Specify the search target (page, post, collection)
├── _config.yml                	# sample configuration
└── index.html                 	# sample home page (blog page paginated)
```

## Default Files

Here are the main files for reference:

### Featured images


### Thumbnails

#### Arts
- Literature
- Cinema
- Music
- Photography

#### Tech
- Desktop
- Technology
- Gadgets
- Gear
- Coding

#### Other Interests
- Sports
- Business
- Travel
- Miscellaneous

