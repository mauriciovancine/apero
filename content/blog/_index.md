---
title: Blog
description: |
  Este é meu blog, onde compartilho meus aprendizados sobre R, Python, Julia, Linux, geoprocessamento, o universo e tudo mais...
author: "Maurício Vancine"
show_post_thumbnail: true
thumbnail_left: false # for list-sidebar only
show_author_byline: false
show_post_date: true
# for listing page layout
layout: list-sidebar # list, list-sidebar, list-grid

# for list-sidebar layout
sidebar: 
  title: Blog
  description: |
   Este é meu blog, onde compartilho meus aprendizados sobre R, Python, Julia, Linux, geoprocessamento, o universo e tudo mais...
  author: "Maurício Vancine"
  text_link_label:
  text_link_url: /index.xml
  show_sidebar_adunit: false # show ad container

# set up common front matter for all pages inside blog/
cascade:
  author: "Maurício Vancine"
  show_author_byline: true
  show_post_date: true
  show_comments: true # see site config to choose Disqus or Utterances
  # for single-sidebar layout
  sidebar:
    text_link_label: Veja os posts recentes
    text_link_url: /blog/
    text_series_label: "In this series" 
    text_contents_label: "On this page"
    show_sidebar_adunit: false # show ad container

---

** No content below YAML for the blog _index. This file provides front matter for the listing page layout and sidebar content. It is also a branch bundle, and all settings under `cascade` provide front matter for all pages inside blog/. You may still override any of these by changing them in a page's front matter.**
