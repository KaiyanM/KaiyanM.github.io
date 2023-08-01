---
title: "Muti-Omics Package Review"
date: 2023-07-31T16:34:30-04:00
categories:
  - blog
Tags:
  - Jekyll
---

## Hi there! 

This is my first post generated with the Jekyll Minimal Mistakes. Whoo-hoo!

I spent some time dealing with the Latex-not-showing issue for multiple plugins, like Jekyll-spaceship and KaTeX. The problem was that since the theme was remotely called from the original template, I could not access the local files for `_layout,` `_includes,` etc. That makes it hard to rewrite the `.html` files to implement text editors. (Of course, copying the repository to local and rewriting does not work.) 

Eventually, the [solution](https://www.janmeppe.com/blog/How-to-add-mathjax-to-minimal-mistakes/) from Jan Meppe helped me out. It provides a way to override other included files in the remote theme, but one hidden trouble is that future updates of the original repo could cause a break to our website. (I think that will be fine since the repo has not been updated for four years...Anyway.)

Now the formula can be easily shown.

$$ \nabla_\boldsymbol{x} J(\boldsymbol{x}) $$

## About The Skin

Have fun with color palettes! I drew a new profile photo and set my own templates for a pleasant workspace. Hope you'll like it too!