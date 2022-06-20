---
step: 4
permalink: /workshop/dhsi/day3.html
video: 4TqpTKZy-hE
title: Day 3 - Understanding the Structure and Workings of CollectionBuilder/Jekyll 
shorttitle: Day 3
overview: "A look into how Jekyll and CollectionBuilder work, and how to use Markdown to write with CollectionBuilder collections."
---
## Day 3: Wednesday, June 9

**Topics**: YML, CSV, Markdown, Liquid Includes, Jekyll Layouts, Bootstrap

### Major Learning Objectives: 

**Conceptual** 
- Understand the difference between CollectionBuilder and Jekyll 
- Understand the nested ('russian doll') nature of a Jekyll project
- Be familiar with Markdown and how one can use it to interpret CollectionBuilder exhibits*

**Technical** 
- Be able to edit and add to your collection’s metadata and objects
- Be able to customize your collection's pages using the config files available.
- Be able to reconfigure the home page layout using _layout/home_infographic.html
- Know how to write an about page and include an image from your collection.*

### Day 3 Workshop Recording:

[https://youtu.be/4TqpTKZy-hE](https://youtu.be/4TqpTKZy-hE)

### Day 3 Outline:

1. Review process of editing CollectionBuilder repository on your computer
-  Answer questions related to this process and last night’s homework

2. Quick insert -- how to clone directly from GitHub Desktop

3. CollectionBuilder components and design overview - [slides](https://docs.google.com/presentation/d/1mLSM2ed9HXxxezyON4IIL3P0bHyOpy0gvbMzFj5R19I/edit?usp=sharing) (Evan)

4. Demonstrate how to add new items and make changes to metadata in Google Sheets, and add the revised metadata CSV to your repository [https://collectionbuilder.github.io/cb-docs/docs/metadata/uploading/#update-metadata](https://collectionbuilder.github.io/cb-docs/docs/metadata/uploading/#update-metadata) (Olivia)

5. How Jekyll Builds the Home page - [bullets](https://docs.google.com/document/d/1zMLxa6J4VMDvXwWNNPmaokaTYHAzS2WevyO25Je3tWM/edit?usp=sharing) \ [model](https://docs.google.com/presentation/d/1iaUD9RCCJg72Nwb6Wal_-4AfHBYWUoDeGs3wMwq6acs/edit?usp=sharing) (Devin)
-  Jekyll [Layouts](https://jekyllrb.com/docs/layouts/) (_layouts/home-infographic.html)
-  [Bootstrap columns](https://getbootstrap.com/docs/4.6/layout/grid/)
-  [Liquid Includes](https://shopify.github.io/liquid/) in layout
-  [TimelineJS](https://timeline.knightlab.com/) include on home page (_includes/feature/timelinejs.html)

6. Begin Customizing About page (Evan) 
-  Introduce Markdown (headers, paragraphs, links, lists)
-  Introduce [Liquid Includes](https://jekyllrb.com/docs/includes/)
  -  Add an image (_includes/feature/item-figure.html)
  -  Add a card (_includes/feature/card.html)
  -  Update About nav (_includes/feature/nav-menu.html)

### Homework

**Continue customizing your collection, add content to your collection’s About page, and customize the layout of the Home page**

1. Finish up any site customization using the _data/theme.yml and _data/ config CSVs.
-  Customize your site using _data/theme.yml: [https://collectionbuilder.github.io/cb-docs/docs/theme/](https://collectionbuilder.github.io/cb-docs/docs/theme/)
-  Customize your site using the config CSVs in the _data folder: [https://collectionbuilder.github.io/cb-docs/docs/customization/](https://collectionbuilder.github.io/cb-docs/docs/customization/)

2. Customize your Home page layout by moving around/deleting/adding includes and changing the Bootstrap grid: [https://collectionbuilder.github.io/cb-docs/docs/pages/home/](https://collectionbuilder.github.io/cb-docs/docs/pages/home/)

3. Add some content to your About page. At the very least we’d like you to create the following content in markdown. Follow the documentation for help: [https://collectionbuilder.github.io/cb-docs/docs/pages/interpretive/](https://collectionbuilder.github.io/cb-docs/docs/pages/interpretive/):
-  Write two paragraphs about your collection ([https://evanwill.github.io/_drafts/notes/markdown-minute.html](https://evanwill.github.io/_drafts/notes/markdown-minute.html))  
-  Create a list
-  Add an include of your choice ([https://collectionbuilder.github.io/cb-docs/docs/pages/interpretive/#feature-includes](https://collectionbuilder.github.io/cb-docs/docs/pages/interpretive/#feature-includes)) 

4. Play around with changing the collection’s look and feel by altering the following (but don’t feel obligated to make these changes permanent):
-  Built-in Bootswatch themes: [https://collectionbuilder.github.io/cb-docs/docs/theme/advanced/#bootswatch](https://collectionbuilder.github.io/cb-docs/docs/theme/advanced/#bootswatch)
-  Font family and size: [https://collectionbuilder.github.io/cb-docs/docs/theme/advanced/#theme-fonts](https://collectionbuilder.github.io/cb-docs/docs/theme/advanced/#theme-fonts) 

5. Continue to practice Git by pulling, committing, and pushing your work. 

6. Get in touch if you run into any issues or have any questions!