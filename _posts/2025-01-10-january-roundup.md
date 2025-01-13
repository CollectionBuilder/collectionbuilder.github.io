---
layout: post
title: 'CollectionBuilder Bulletin: January 2025'
subtitle:
author: Devin Becker
publish-date: January 10, 2025
tags: [newsletter]
short_description: 'A round-up for January 2025.'
---
Hi Everyone, 

We have **a lot of updates** with the new year. The team went for a retreat in 
November to beautiful McCall, Idaho. Evan made us watch a hockey game (which ended up being amazing) and we got a lot of work done, both on the core of CollectionBuilder and on some new features. 

And then in less fun news, Evan's been discovering issues with an update to the GitHub Actions Jekyll workflow that builds CollectionBuilder-CSV websites on GitHub and with the latest Ruby update. No worries we have fixes (see below), but both issues will likely cause some frustration unfortunately. 

As always, If you have a project and/or event you’d like us to highlight next month please email [collectionbuilder.team@gmail.com](mailto:collectionbuilder.team@gmail.com).

\- The CollectionBuilder Team (Devin writing this ...)

## **This month’s news:**

### We took a retreat!

The CollectionBuilder Team took a short retreat during which we worked on some long standing issues and developed some new features.  

**Boring (but Important) Updates to CB-CSV:** The CollectionBuilder-CSV repository received several minor, non-breaking updates last week during a team retreat, including:  

- normalized and documented Index includes
- a significant reorganization of Rake tasks into a dedicated "rakelib/" folder for improved manageability. 
- Several new utility tasks were also added for working with objects, including download_by_csv, rename_by_csv, rename_lowercase, and resize_images, with corresponding documentation available in the "docs/rake_tasks" directory.

These updates are currently only available in the main branch of CB-CSV and are intended for new projects, with no need to update existing implementations unless new functionality is desired. While more substantial changes with breaking updates are in development, these modifications are currently exclusive to CB-CSV, with plans to eventually roll out compatible changes to CB-GH and CB-Sheets platforms.

**Exciting updates!:**

We also built some cool things, several of which are not quite ready for prime time (but email us if you want to live dangerously): 
    
- ***a new gallery feature*** -- this feature will allow you to create a gallery on any CB page, with options for a featured image at the top. The include lets you filter your collection to a curated group of items from your collection. 
    - This came out of work on a DHSI collection this past summer by Briar Pelletier. She added several galleries of prints based on the year they were featured. [See 2016 here!](https://briarpelletier.github.io/maps-archive/galleries/2016.html)
- ***a revised about page*** -- Olivia is working on a major revision of the about page that automatically generates a table of contents at the top right and changes the basic size of the text block. It looks a lot better and we're excited to roll that out this spring. 
- ***a cb-essay repository***-- I've been working on a repository that takes some of Evan's work on [Fire Lines](https://cdil.lib.uidaho.edu/fire-lines/) and some of my work with a recent CDIL fellow (CDIL is our DH center at the University of Idaho) that will help people use CollectionBuilder to publish long form essays with a collection underneath. There will be options for stepping through the essay and also for a scroll-based experience -- you can see a example of how that should work in [an essay on our new project Keeping Watch](https://cdil.lib.uidaho.edu/keeping-watch/essay/).

### There are two breaking issues (not our fault!)

Two new issues that CB users are probably encountering: 

- An update to GitHub Actions is causing build errors that impact anyone using the default "jekyll.yml" workflow--i.e. if you are building CB-CSV on GitHub, you are probably impacted! Check the [GitHub Actions Bug blog post for fixes](https://collectionbuilder.github.io/2025-01-09-gh-pages-issue/)
- Jekyll is having issues with the most recent Ruby versions. The CB-CSV template's "Gemfile" has been updated to fix the problem, but you may encounter errors if building an older project with a fresh Ruby install. Check the [ blog post for info](https://collectionbuilder.github.io/2025-01-08-gemfile-update/).

## **Get Involved / Connect with Us**

Below are some ways to stay connected with the CollectionBuilder community:  
* [Join our Slack channel](https://forms.gle/GVb7STSWyq2tto3NA)  
* Post questions on our [GitHub Discussion Board](https://github.com/orgs/CollectionBuilder/discussions)  
Questions? Email us at [collectionbuilder.team@gmail.com](mailto:collectionbuilder.team@gmail.com)   

