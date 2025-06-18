---
layout: post
title: 'LIS Student Reflection: Diamond Alexander, Denver University'
subtitle:
author: Diamond Alexander
publish-date: June 24, 2024
tags: [student-reflection]
short_description: 'LIS Student Program participant Diamond Alexander reflects on her time in the LIS Student program and releases a collection of personal, upsetting, cringey, wacky, and eye-roll worthy moments from women’s bowling in the United States.'
---

MLS Student Diamond Alexander answers a series of questions on the collection she built for the LIS Student program and the program overall. Diamond was one of the participants in the [2024 LIS Student Program](/community/student-incentives.html){:target="_blank" rel="noopener"}. 

{% include feature/blogbio.html bio="Diamond Alexander is a Librarian-in-Residence at the Library of Congress and a recent graduate of the University of Denver's MLIS program. Some of her professional interests include usability/accessibility, linked data, and user experience design. In her spare time, Diamond enjoys baking, crocheting, reading, as well as sight-seeing and spending time outdoors. " img="/images/blog/biopics/Diamond-Alexander-headshot.png" name="Diamond Alexander" %}

# LIS Student Program Spotlight: Diamond Alexander

### Please describe the CollectionBuilder project(s) you worked on during the LIS Student Program and provide a link to your projects if available. 

[My project](https://collectionbuilder-lis.github.io/striking-form/) is titled “Striking Form” and it is a digital exhibit showcasing a selection of personal, upsetting, cringey, wacky, and eye-roll worthy moments from women’s bowling in the United States. It began as a way for me to display my great-grandmother’s bowling ephemera but as I learned about women’s bowling in the US, I expanded my project’s scope to include other images and newspaper clippings to tell a bigger story about the sport.

**Link to project: <https://collectionbuilder-lis.github.io/striking-form/>**

### What were some of the benefits and/or successes of using CollectionBuilder for your project(s)? What were some of the limitations or drawbacks?
Some of the most significant benefits that come to mind are:

- CollectionBuilder’s emphasis on metadata quality. The major functional components of CB rely on well-done metadata so writing good records and performing quality assurance on them helped me strengthen the theoretical foundation I had gained from coursework.
- Particularly with CB-CSV, the flexibility of the metadata. The metadata fields are highly customizable so a lot can be done on a site without the need for additional plugins or sophisticated code.
- Customization of the “look and feel.” I came into the LIS Cohort with some previous HTML/CSS experience and that helped me easily envision what little tweaks I wanted to make here and there. If I hadn’t had that background, I think I could’ve gotten the help I needed from either the CB community or elsewhere on the web since the front-end is built using the wildly popular Bootstrap framework – another one of the benefits of CB.
- Hosting my site using GitHub Pages has been a breeze so I definitely count that as a success.

### What were some of the challenges you faced while using CollectionBuilder? How did you navigate these challenges?

- At the beginning, I think my biggest challenge was diving into all of the fun options and settings within CollectionBuilder before I had my objects and metadata finalized. I think starting with a small number of objects, which I did, was wise but instead of then jumping into making customizations, I should’ve gone back and finished inputting all of my metadata first.
- One challenge that I encountered throughout my time using CB was navigating the folder/directory structure of my project. This was my first time working with a static-site generator so I was unfamiliar with the overarching system of organization used for the different files and folders. This meant when I was looking to make extensive changes to my project’s Browse page, for example, there were a few different files I needed to edit and they weren’t all in the same place 😭 [This page on template structure](https://collectionbuilder.github.io/cb-docs/docs/advanced/architecture-overview/) from the CB Docs would have come in handy had I found it earlier in the process.
- While CB being powered by good metadata is a benefit, the downside is that any aberrations in the metadata (.e.g there’s an extra space where it shouldn’t be) certain parts of the site won’t function properly or show up at all – and it might not be immediately clear it’s an issue with the CSV. Thankfully, the CB Team has enumerated many of these potential issues on [this page about formatting](https://collectionbuilder.github.io/cb-docs/docs/metadata/formatting/). This happened to me with my subjects and locations “word cloud” pages and eventually, I think I realized it was a combination of me changing the variable name for “subject” in one of the config files and badly formatted subjects in my CSV.

### What advice do you have for others wanting to use CollectionBuilder?
CollectionBuilder is incredibly fun to work with so my first piece of advice is to dig in. Gather ~5 objects to start with – they could be books from your shelf or photos of items on your desk – and once you have the bare minimum metadata fields filled out, start playing around with the CB configuration settings. With just a few tweaks, you can change colors, typography, and text! Refer back to the template structure overview page and then just systematically start looking through the folders and look at what each file does.  

From here, I recommend thinking about the purpose of the site. This will help inform decisions such as which cards, if any, you want to have on the homepage or how much metadata to display on an item page vs. the downloadable files, as a few examples. Knowing your project’s purpose also helps prevent overwhelm because you’ll have narrowed down any potential customizations to just the ones that will benefit your specific use case.

My last piece of advice is for those who want to implement a high degree of customization: get familiar with Bootstrap’s docs and look for inspiration around the web. Knowing what components and styles are available to you can give you the confidence to push the bounds of the CB base template. I started to do a bit of this toward the end of the LIS Cohort and made a number of changes to my project’s Browse page that differ from the base template: I changed the item cards, search bar layout, and even how my items sort on page load.


{% include feature/image.html objectid="/images/blog/cb-browse.png;/images/blog/striking-browse.png" caption="A typical CollectionBuilder Browse Page; The revised version in Striking Form" link="https://www.lib.uidaho.edu/digital/psychiana/browse.html;https://collectionbuilder-lis.github.io/striking-form/browse.html" target=true%}


### Do you have any future CollectionBuilder projects that you are planning to do? If so, please describe them.

I will be starting a new job soon so honestly, all of my fun side projects have been put on pause until I settle into my new role. However, I saw someone used CB for a rocks & minerals collection and it looked so cool to me! That gave me the idea to try something similar with my yarn collection since yarn skein labels have SO MUCH metadata on them and I could see myself having fun pulling in images of the [yarn weight symbols from the Craft Yarn Council](https://www.craftyarncouncil.com/standards/yarn-weight-system), for example, onto the item pages or getting creative with filter dropdowns, etc.

### Do you see yourself using CollectionBuilder in your future career? If so, how would you implement it in your work?

My hope is to work with digital technologies in a library setting so I absolutely could see myself either using CB myself or advocating for its use in my future career. I think it’s a valuable tool not only for creating collections but for naturally improving the tech literacy and capabilities of anyone who uses it. I would love to see it included as a digital resource on academic library LibGuides guides or advertised as a tool in digital humanities library initiatives.

### Anything else to add? Please feel free to comment on your overall experience in the LIS Student program, and/or to share links to any projects, repositories, etc.

One of my favorite moments was when I finally organized my metadata template the way I wanted and got to see all of my items populate on the Browse page for the first time. It was very satisfying to have a visual representation of what was previously just a long page of comma-separated values in my code editor! That is the power of CollectionBuilder.

Overall, I feel super lucky to have been a part of this cohort and am confident that what I’ve learned by participating in it will serve me throughout my career in myriad ways.


