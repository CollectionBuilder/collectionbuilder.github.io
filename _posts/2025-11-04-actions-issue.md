---
layout: post
title: 'GitHub Actions Issues with CB-CSV'
subtitle:
author: Evan Williamson
publish-date: November 04, 2025
tags: [alert, tech, ruby-jekyll, cb-csv]
short_description: 'Tweak your jekyll.yml to avoid build errors.'
---

Folks have been encountering a build error when using the default "jekyll.yml" GitHub Action with fresh CollectionBuilder-CSV projects, with an error message something like:

`The process '/opt/hostedtoolcache/Ruby/3.1.6/x64/bin/bundle' failed with exit code 5`

There is some sort of dependency hell issue with the Sass requirements and the older Ruby version the default Action uses.

The best solution is to manually update the Ruby version specified in the "jekyll.yml":

- In your project look for the file ".github/workflows/jekyll.yml".
- Edit around line 40 where it says `ruby-version: '3.1'`, updating it to `ruby-version: '3.4'`

That should fix the build! 
(Let us know if you encounter issues...)
