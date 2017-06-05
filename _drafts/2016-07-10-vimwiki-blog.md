---
layout: post
title:  "Using vimwiki for blogging"
date:   2016-07-10
categories: vimwiki blog
---
Since I'm going to start using vimwiki to record my personal dev diary, it makes sense to use these
posts in a blog. I have a github.io blog using Jekyll which I never post to because it's too much
work. Since vimwiki reduces the friction in creating diary posts, why not use these posts in the
blog? Both use markdown style syntax, and it may be possible to automate this.

After looking a bit into this, I have come up with an initial workflow:

* Create daily diary post with vimwiki. This saves posts by default in ~/vimwiki/diary/(datestamp).wiki.
* Created a symlink within the Jekyll blog folder, linking to the diary folder.
* .gitignore has .wiki files added, so the diary posts aren't accidentally added to the github repo.
* Copy desired diary posts from diary folder into the Jekyll posts folder. Rename the file from .wiki --> .md, and add title to the filename, e.g. 2016-07-09.wiki --> 2016-07-09-post-name.md
* Add Jekyll header to beginning of post (layout: post, title: "title", etc).
* Scrub / edit differences in markup. There are some differences between vimwiki and Jekyll.
* Test locally with jekyll serve, etc

It seems like a lot of steps, but if content is already typed up, it's really just copying / renaming
the post, and adding the Jekyll header. Then after that, it's just testing and adjusting formatting,
which would be needed regardless anyway. Still, if possible, it would be better if I could automate
the process more. Maybe have a script which takes the == vimwiki heading == and adds it to the
filename, while renaming the file, and adding a placeholder Jekyll header.

Anyway, I'll see how well this works.

Edit: I shouldn't have committed the symlink up to the repo. Jekyll serve ran ok locally but when
it was posted to github.io, it choked. I git rm'ed the symlink from the repo to fix it. For
convenience, I still have the symlink locally for easy file copying, etc. and have added it to the
gitignore.
