---
layout: post
title: 'Jekyll Issues with Ruby 3.4.0+'
subtitle:
author: Evan Williamson
publish-date: January 08, 2025
tags: [alert, tech]
short_description: 'Update your Gemfile to avoid Jekyll issues with latest Ruby releases.'
---

As of January 2025, if you are running the most recent stable Ruby version (3.4.0+) and the current version of Jekyll (4.3.4), you might encounter errors when using `bundle install jekyll s` on existing projects!

There is a bunch of changes to the standard library in the new versions of Ruby (3.4.0+).
The current version of Jekyll hasn't caught up with adding all the requirements to their dependencies yet, so if you are running a recent version of Ruby you may be getting a lot of warnings messages in the terminal--or worse, if you have the fresh current stable version ruby 3.4.1, you will get weird error messages on `bundle exec jekyll s` and it won't run at all. 

The required dependencies are now added the the CB-CSV "Gemfile" (as of Jan 8th, 2025), so fresh collections should be fine! 

If you run into the issue with an existing project (on your freshly installed new ruby): 

- Delete the "Gemfile" and "Gemfile.lock" in your repository
- Add a copy of the new ["Gemfile" from collectionbuilder-csv](https://github.com/CollectionBuilder/collectionbuilder-csv/blob/main/Gemfile)
