---
title: Setting up the blog
author: Angela
date: '2018-11-30'
slug: setting-up-the-blog
categories:
  - blogdown
tags: [blogdown deploying ]
---
I am referring primarily to the Blogdown book by Yihue to build this website.
I am also working off Alison Premane Hills tutorial 'Up and Running with blogdown. A workshop for the Portland R User Group'.
[slides and link]("https://apreshill.rbind.io/talk/blogdown-meetup/")

## `blogdown::new_site()`  
command to build a site

## `serve_site()` 
I need to find out when to use `serve_site()` instead of `hugo_build()`
serve_site() seems to do the trick for me. When I run this command, I then can drag my public folder directly into the netlify page to manually deploy it.

## adding a logo
Adding a logo. The logo file is kept in the /static/ folder
save your logo image into the static folder. in the config.toml file go down to [params.logo] and change the default url to the name of your image to be used as the logo. in my case "rocco2.png"

## choosing a theme

I have considered various themes to try out by looking at some other blogs. Some of the ones that I like are `Beautiful Hugo`, `Blackburn` and also `Academic` but I feel that I am not academic enough to be using `Academic`!
What I want is a simple page where I keep my learning efforts / posts and be able to find them easily. The `Academic` theme seems to have a section with a menu on the right that is easy to navigate. I could just remove the sections that are not relevant to me.


## continuous deployment 
I had problems on an earlier version of the blog where continuous deployment was failing. For this version I started a new project using the git version control option and copied the git repository url into the first field. 
This was the url from the new repository on github that I also used in terminal `got clone repository url`

## modifying the site layout

While I like the Academic theme, there are many sections that are not relevant to me as I am a learner rather than a teacher.
I am therefore modifying the layout to remove the pr-edefined sections such as Teaching, Publications, Recent and Upcoming Talks, Biography. I have to play around with it to figure it all out. The layout is specified in the `config.toml` file while the contents are under content / home.
I can add sections I presume following the same format and file system.
I have deleted several of the included files in the `content/home` folder. Specifically talks.md, teaching.md, talks_selected.md, skills.md, publications.md, publications_seleted.md, contact.md, experience.md

I added a new section by essentially copying the `teaching.md` file which is an example of using the `custom` widget to create your own homepage section

I amended the contact widget in `contact.md` active = false. I also set active= false in the `hero.md` file

## latest site update

I am happy enough now that I have the blog up and running. There are a few more modifications I will make to personalise the site.
I am happy that the continuous deployment is working on netlify.