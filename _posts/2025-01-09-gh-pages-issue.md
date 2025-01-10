---
layout: post
title: 'GitHub Actions Bug!'
subtitle:
author: Evan Williamson
publish-date: January 09, 2025
tags: [alert, tech]
short_description: 'Issue with GitHub Actions can cause errors building sites.'
---

As of January 2025 there is a *currently a bug in the default GitHub Actions "jekyll.yml" starter workflow!*

Due to [changes in the ubuntu-latest image](https://github.com/actions/runner-images/issues/10636), the GitHub Action will end up with errors in existing and new repositories using the workflow--i.e. if you set up a CB-CSV site and are building it with the default GitHub Actions, new builds will likely fail with errors going forward! 

Please note that we do not maintain the "jekyll.yml" or GitHub Actions so can not directly fix the default starter workflow. 

To fix it in your project, edit the file ".github/workflows/jekyll.yml" in your repository. There is two possible ways to fix it.

The first option is to update the `setup-ruby` version.
On line 37, replace:

`uses: ruby/setup-ruby@8575951200e472d5f2d95c625da0c7bec8217c42 # v1.161.0` 

with: 

`uses: ruby/setup-ruby@v1.207.0`

This should fix the error!

*Alternatively*, the second option is to roll back the image used by your action. 
On line 32, replace:

`runs-on: ubuntu-latest`

with: 

`runs-on: ubuntu-22.04`

This will restore it to the older image which still works correctly.

*(you only need one of these options to fix the issue!)*

There is an [Issue in the CollectionBuilder-CSV repository](https://github.com/CollectionBuilder/collectionbuilder-csv/issues/96) and a note in the [documentation](https://collectionbuilder.github.io/cb-docs/docs/deploy/actions/) tracking this problem.

Eventually, we assume someone will fix the default "jekyll.yml"... However, existing repositories may require this manual fix.
