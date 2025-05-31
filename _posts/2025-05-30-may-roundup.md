---
layout: post
title: 'CollectionBuilder Bulletin: May 2025'
subtitle:
author: Devin Becker
publish-date: May 30, 2025
tags: [newsletter]
short_description: 'May 2025 Updates: New Browse! New About!'
---
Hi Everyone, 

So when we did our first workshop ever for CollectionBuilder—DLF Tampa 2019! —we were still throwing everything together for our platform and documentation on the plane. None of this work really mattered when the workshop started, however, because we also tried to have everyone download and install all the software to run CB, including Ruby, and that was its own disaster. 

We were all reminded of this story today as we frantically added some new features to CollectionBuilder-CSV, **including a revamped Browse page with advanced search and a redesigned About page with an automatically generated table of contents (links below)**, before Evan and Olivia leave to go teach in Montreal at DHSI this coming week. 

Luckily, our docs page is well-established and making changes and adding documentation is much smoother. We're so advanced now that we even have a blog and listserv to announce these changes! 

So yay us. It's only taken like 6 years... 

But it is really exciting to announce these changes, as the revamped Browse features are something we've been asked about for a long time and the new About page design was a loooong time coming. 

More details below and hope you enjoy!!

\- The CollectionBuilder Team


## This month's news:

**New Advanced/Faceted Search and Default Sort for Browse Page!**: CollectionBuilder-CSV now offers enhanced browse functionality with powerful new search and filtering capabilities. Users can access detailed search options through an advanced search modal, while a new faceted search panel allows filtering results by specific metadata fields configured in your collection. Additionally, collections can now specify a default sort field to control the initial order when users first visit the Browse page. These features are easily controlled through new options in `_data/theme.yml`, giving collection creators fine-grained control over their users' browsing experience. 
- [Check out the Demo Version](https://compound-1lqv.onrender.com/browse.html)
- and a [more complex version (details below)](https://www.lib.uidaho.edu/digital/taylor-archive/browse.html) 


**Redesigned Browse Page!**: The About page has received a significant redesign featuring an auto-generated table of contents and refreshed layout that improves both mobile and desktop viewing experiences. This update includes new front matter options for featured images and improved responsive design, along with component updates across various feature includes like cards, videos, modals, and accordions to align with the new design standards. The redesign maintains CollectionBuilder's clean aesthetic while providing better navigation and visual consistency throughout the collection interface.
- [Check out the Demo Version](https://compound-1lqv.onrender.com/about.html)

**GH and SHEETS Updated with CSV Features**: While the above Browse and About updates haven't made it yet, CollectionBuilder-GH and CollectionBuilder-Sheets did receive important updates pulled from CollectionBuilder-CSV, including the auto-center map option, feature include improvements, accessibility fixes, and general tweaks. While not all CSV updates are compatible with the GH version, these updates help keep the templates more aligned. Notably, the Gemfile for both CB-GH and CB-Sheets has been updated to include the "github-pages" gem, which keeps projects in sync with GitHub Pages' actual build environment—this gem is now compatible with Ruby 3+ after previous incompatibility issues, so remember to run `bundle install` when starting new projects!


## Newly Released Wilderness Research Collection Features new Browse and About pages!

- Our new [Taylor Wilderness Research Station Archive](https://www.lib.uidaho.edu/digital/taylor-archive/) features video interviews, archival documents, artifacts, research outputs, and other photographs and ephemera collected from Taylor Ranch, which the University of Idaho promotes as the world's "wildest classroom." Taylor is deep in the heart of the Frank Church-River of No Return Wilderness and surrounded by 2 million acres of wilderness. This collection has some really great visualizations in it, including some developed with Google Earth Studio. And it also features our new About Page design and provides a good collection to check out our new browse functionality, since the archive is large and complex. 
   - [Check out the Browse Page](https://www.lib.uidaho.edu/digital/taylor-archive/browse.html)
   - [Check out the new About Page design](https://www.lib.uidaho.edu/digital/taylor-archive/about.html)




## **Get Involved / Connect with Us**

Below are some ways to stay connected with the CollectionBuilder community:  
* [Join our Slack channel](https://forms.gle/GVb7STSWyq2tto3NA)  
* Post questions on our [GitHub Discussion Board](https://github.com/orgs/CollectionBuilder/discussions)  
Questions? Email us at [collectionbuilder.team@gmail.com](mailto:collectionbuilder.team@gmail.com)   

