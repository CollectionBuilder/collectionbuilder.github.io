---
title: DHSI Coursepack
permalink: /workshop/dhsi/full.html
layout: page
---
Course Details

# Creating Digital Collections with Minimal Infrastructure: Hands On With CollectionBuilder for Teaching and Exhibits.

This document may change as we progress through the week. The living version of this document can be found here: [http://bit.ly/cb-dhsi2021](http://bit.ly/cb-dhsi2021)

Dates: **7-11 June 2021**

Class Time: **12:00pm - 1:30pm Pacific**

Office Hours: **2:00pm - 3:00pm Pacific** everyday, or by appointment (email us!)

Location: Zoom! (Zoom information will be emailed to participants shortly before the course begins)

Instructors:

* Olivia Wikle ([omwikle@uidaho.edu](mailto:omwikle@uidaho.edu))

* Evan Williamson ([ewilliamson@uidaho.edu](mailto:ewilliamson@uidaho.edu))

* Devin Becker ([dbecker@uidaho.edu](mailto:dbecker@uidaho.edu))

# Course Description

Build your own digital collection in a week! Learn fundamental web and DH skills working with CSV data and digital files to generate websites that allow users to visualize and browse digital collections in multiple ways.

CollectionBuilder is an open source project for building digital collection and exhibit websites driven by metadata and hosted on lightweight infrastructure. The high cost and IT requirements of digital collection platforms are often a barrier to creating new collections for sharing or teaching humanities research. CollectionBuilder is optimized for non-developers and simple hosting solutions, allowing researchers and educators to take greater ownership over their digital projects and lowering barriers to website customization. Using well-structured metadata and a directory of digital files, CollectionBuilder employs a Jekyll static web generator to create a website for visualizing, browsing, and accessing the collection.

As workshop participants engage with CollectionBuilder, they will learn fundamental web and DH skills by working with plain text files, CSV data, Markdown, GitHub, and GitHub Pages to create and customize their very own digital collection. By the end of this workshop, participants will have gained the knowledge and independence necessary to implement CollectionBuilder in contexts that include creating and disseminating research collections and custom digital exhibits, or teaching digital libraries in the classroom. No programming experience is necessary; beginners from any background are welcome. Participants are asked to bring their own computers.Code of Conduct

# Code of Conduct

We are committed to creating a respectful learning environment that is inclusive of participants with all backgrounds and abilities. This course will adhere to the [DHSI Statement of Ethics & Inclusion](https://dhsi.org/statement-of-ethics-inclusion/), and the [CollectionBuilder Code of Conduct](https://github.com/CollectionBuilder/collectionbuilder.github.io/blob/main/CODE_OF_CONDUCT.md). 

By engaging with the methods of creating digital collections that will be introduced in this course, participants will become valued members of the CollectionBuilder community, a primary goal of which is to be inclusive to contributors with varied and diverse backgrounds. As community participants, we pledge to make participation in our project and community a respectful and harassment-free experience for everyone, regardless of age, body size, disability, ethnicity, sex characteristics, gender identity and expression, level of experience, education, socio-economic status, nationality, personal appearance, race, religion, or sexual identity and orientation.

We invite all those who participate in the CollectionBuilder project and community to help us create safe and positive experiences for everyone.

# Course Objectives

By the end of the course, we hope you will: 

* Understand how static website generators work and what advantages and disadvantages they offer.

* Be familiar with the base functions and customizable options that CollectionBuilder offers through its various templates.

* Be comfortable using a development environment to build static sites. 

* Build one customized and polished digital collection and understand how and where you could publish the collection online.

* Be able to teach or introduce CollectionBuilder and Jekyll to others.

# Course Software & Data

One of the more challenging parts of working with data and the web is getting a development environment set up that you understand and that makes your work easier. We believe the environment we use to develop with CollectionBuilder is pretty good, but even amongst the three of us we disagree on some of the components. This week we will be teaching you how to set up a development environment like ours, but the most important part is that you feel comfortable and enabled by the tools and software you use to build the sites. Below are links and short details to the tools/software we use to develop CollectionBuilder. 

Please use our CollectionBuilder documentation for help with installing all these pieces:  [https://collectionbuilder.github.io/cb-docs/docs/software/](https://collectionbuilder.github.io/cb-docs/docs/software/) 

## Spreadsheets for Metadata Management

With CollectionBuilder, Everything starts with metadata, so it's important to have reliable means for working on, collaborating, and transforming your data. We use Google Sheets because we find that it's the easiest platform to collaborate on and, unlike Excel, it does less automatic transformations on one's data. Google sheets also facilitates an easy download of the data into a CSV format. Collection data must be in a CSV format for CollectionBuilder to process it, and we've found Sheets is reliable for this (Excel can not save a correctly formatted CSV). 

For more complicated projects, we also use Open Refine, which is excellent with data transformations. But for this class and this level of project, Google Sheets should be fine. If you would prefer a desktop alternative, [LibreOffice](https://www.libreoffice.org/) Calc is a good free and open source spreadsheet program that will handle encodings and CSVs correctly. 

## Text Editor - Visual Studio Code

We use Visual Studio Code, an integrated development environment (IDE). VS Code is a free, open source Microsoft product, and quite popular with developers worldwide. VS Code allows for easy access to the project’s file structure, as well as a terminal and text editor all in one screen. Other text editors (Atom, for instance) will work fine as well, but we're most familiar with this one and have found it to be user-friendly and increasingly powerful as one gets better acquainted with its many features and plugins. One plugin we'll have you download right away is Rainbow CSV, which adds color cues to CSV files that are displayed in the system.

## Version Control Software (Git + GitHub)

Git is the most popular version control software, and is free and open source. We use Git to track the development of our projects and to assist us with collaborating. It's important to note that Git is different than GitHub, which is a platform that uses Git to enable collaborative software development. Git is the software that enables one to track differences in file versions. GitHub is a platform that uses Git to enable collaborative development and online publication of the git process and web outputs. We use GitHub, but one could use GitLab, BitBucket, or other repository hosts in a similar way. 

We will show you how to use Git and GitHub on the web interface and on your local computer.  Locally, some find working through VS Code's built-in version control features helpful, and some of us like using GitHub Desktop to manage the various git commands and tasks. We'll show you both. 

## Static Site Generator (Jekyll, a generator written in Ruby)

Jekyll is an open source static site generator that runs on the Ruby programming language. Overall, Jekyll has been kind to us, but Ruby is really annoying. (Just kidding, Ruby, you're great!). Really, once you have Ruby set up correctly, there are few problems. But sometimes getting the right version of Ruby set up and correctly configured can be a pain. We have specific how-to instructions for setting up Ruby on [Windows](https://lib-static.github.io/howto/howtos/installrubywindows.html), [Mac](https://lib-static.github.io/howto/howtos/installrubymac.html), and [Linux](https://lib-static.github.io/howto/howtos/installrubylinux.html). We are also happy to help you during or prior to the class starting (we'd love it if you could get this installed before we start, but we know that might be hard for some!). 

As for Jekyll, we gave a lot of thought to what static site generator to use for CollectionBuilder, as there are [many site generators available](https://jamstack.org/generators/). We came to use Jekyll because the way it represents its code, files and folders made the most sense to us and because it is the most popular version. Here is what we wrote in [one of our articles](https://www.tandfonline.com/doi/abs/10.1080/10691316.2021.1887036) detailing our approach: 

University of Idaho librarians evaluated a wide variety of static site generators, eventually settling on Jekyll for a variety of reasons. First, Jekyll is set up so it supports a simple mental model of how the site will be built that matches up with traditional web development approaches. Static assets in a folder in the source code will become static assets in the same location on the built-out site. Content is represented by stub files that are assigned a layout that pulls together the modular template elements of each web page. This arrangement is similar to the library’s earlier templates of PHP includes, built into a tool that makes the approach considerably more powerful and sustainable. University of Idaho librarians’ experiences teaching others during classes, workshops, and internal sessions suggest that the biggest barrier to getting started with Jekyll is setting up the development environment, including Ruby, the programming language necessary to run it. Once past that initial hurdle, learners without a development background are able to understand how the tool works and web pages are constructed. In contrast, some of the major alternatives, such as Hugo, GatsbyJS, and Next.JS, seem to rely on a more formal computational mental model for constructing sites, making them amenable to JavaScript developers, but less intuitive to an average librarian.

Second, Liquid, the templating language used by Jekyll, is powerful yet easy to learn, opening new possibilities for driving content generation from simple data formats such as CSV. This ability to use data created and edited in spreadsheet formats, allows rethinking much of the website content as re-usable chunks added into pages using flexible templates. Spreadsheets are something library folks have plenty of experience with, providing an easy entry point for collaborators to create, organize, and maintain content on the site.

Finally, Jekyll has become the most popular out of the myriad of emerging static generators. This is in part due to being integrated into GitHub's free web hosting service, GitHub Pages, making it an attractive option for quick projects and learning opportunities. The vibrant community around these tools results in better support when encountering issues and a wide ecosystem of quality examples to draw from.

On the surface, "popularity" might seem like a shallow metric to consider when selecting tools, but it has become a significant factor when evaluating the sustainability and usability of different technology choices. In the library’s context, ready availability of quality documentation and help resources can lower the barriers for learning and use. Additionally, tools such as Jekyll, Bootstrap, and GitHub have huge novice user communities that ask questions and post answers across the web. A quick, specific search will almost always return solutions that are comprehensible to non-computer scientists for any issue one encounters. This accessibility of help resources and a community of users is essential to fostering a library-centric approach as well as keeping the workflow "do-able" for University of Idaho librarians and, the authors argue, for librarians generally.

So yeah, we've given it some thought! 

Again, we know getting these environments set up and making them usable is often challenging. One of our main goals for this class is getting you comfortable using this method of development, so please reach out to us with any issues or problems you might encounter. 

# CollectionBuilder Course Schedule:

This course is designed to include one and a half hours of virtual teaching and discussion per day, accompanied by approximately one hour of homework per day. By course’s end, participants will have created a digital collection with their own material, learned various possibilities for customizing and extending that collection, and discovered the opportunities that CollectionBuilder can provide as a starting point for future DH web development.

## Day 0: Preparation

1. Download and install software (Visual Studio Code, Git, GitHub Desktop, Ruby, Jekyll)
-  Please use our CollectionBuilder documentation for detailed help with installing all these pieces:  [https://collectionbuilder.github.io/cb-docs/docs/software/](https://collectionbuilder.github.io/cb-docs/docs/software/) 
-  All software is free, open source, and cross platform.
-  If you run into problems installing some of this software, don’t despair! You’re welcome to contact us at any point leading up to the workshop and we’ll help you troubleshoot. We’ll also make time during the workshop week to address these issues, so if you don’t get them all installed by Day 1, that’s okay.
-  If you’re interested, see our section above for information about the software we use.

2. If you don't already have one, create a [GitHub](https://github.com/) account and make sure you'll be able to access it during class time

3. This class will involve some editing in Google Sheets, so please be sure to have a working [Google Drive](https://www.google.com/intl/en_zm/drive/) account set up before the workshop begins. (If you do not use Google products, please have LibreOffice Calc available to edit spreadsheets)

4. Watch this short introduction to CollectionBuilder: [https://collectionbuilder.github.io/workshop/gh/introduction.html](https://collectionbuilder.github.io/workshop/gh/introduction.html), and take some time to explore this demo collection: [https://collectionbuilder.github.io/collectionbuilder-gh/](https://collectionbuilder.github.io/collectionbuilder-gh/). 

5. Prep objects for your digital collection
-  Number: 10-30 objects
-  Formats: jpg, pdf, mp3, YouTube, Vimeo
-  Size: GitHub repositories are limited to 1GB, so make sure the total size of your objects folder is less than around 500MB. Secondly, since CollectionBuilder-GH does not use thumbnails, keep your objects to a reasonable size for access on the web. The objects are usually not your full resolution versions. For example, jpg images about 1000px wide and pdfs less than 1 MB will work well. 
-  Location: for easy uploading to GitHub, gather your prepared objects in one folder on your computer. 

6. Prep metadata (**_Optional!_**** – We’ll talk through the metadata fields in class, so don’t worry about this if you don’t have time to prepare your metadata yet.**)
-  Log in to Google Drive. Then, using Google Sheets, make a copy of the [CollectionBuilder-GH metadata template](https://docs.google.com/spreadsheets/d/1Uv9ytll0hysMOH1j-VL1lZx6PWvc1zf3L35sK_4IuzI/edit?usp=sharing) (Use the "make a copy" option under the “File” tab. Note that the “make a copy” option won’t be available to you if you’re not logged in!)
- If you really want to get a head start, you can follow our [metadata guidelines](https://collectionbuilder.github.io/cb-docs/docs/metadata/) to begin filling in the template. Any custom field can be added based on the needs of your project, but column names should be lowercase with no spaces or odd characters.

----------------------------------------------------------------------------------------------------------------------------------------------

## Day 1: Monday, June 7

**Topics**: CollectionBuilder intro, GitHub, working in GitHub web interface

### Major Learning Objectives

**Conceptual** 
- Have a basic understanding of the structure and design of a CollectionBuilder site
- Understand the importance of case in the naming of files and file extensions
- Recognize the required metadata fields for a CollectionBuilder-GH instance
- Understand how to find the CollectionBuilder docs and how to use them*

**Technical*
- Be able to use Google Sheet formulas and filters to fill in your metadata
- Be able to start a CollectionBuilder project using the CollectionBuilder-GH Template
- Be able to recognize a .YML file and where to find a _config.yml file in a Jekyll project*

### Day 1 Workshop Recording:

[https://youtu.be/ZPOKRpxGJqg](https://youtu.be/ZPOKRpxGJqg)

### Day 1 Outline:

1. CollectionBuilder introduction ([https://collectionbuilder.github.io/](https://collectionbuilder.github.io/)) - [slides](https://docs.google.com/presentation/d/1lGTaVdAa3UudvkwlFMAYYLe7J91d2AyHZgpFX47YI5g/edit?usp=sharing) (Devin)
-  Tour a CollectionBuilder demo site

2. Intro to CollectionBuilder docs ([https://collectionbuilder.github.io/cb-docs/](https://collectionbuilder.github.io/cb-docs/)) (Olivia)
-  Documentation sections
-  Documentation search

3. Collection Objects (Evan)
-  Object types
-  File extensions
-  Filenaming conventions and issues

4. Metadata (Devin)
-  Why use Google Sheets?
-  [Required fields](https://collectionbuilder.github.io/cb-docs/docs/metadata/gh_metadata/#required-fields-for-collectionbuilder-gh-and-sa)
-  Google sheets tricks ([Quick Tutorial/Presentation](https://docs.google.com/document/d/1KXQMR4CalRgpF9T_UKDlC-JDvPDorK9E8R838cmhAX8/edit?usp=sharing))
- Formats, filenames, field names

5. Quick demo of setting up a collection (Olivia)
- Copy CollectionBuilder-GH Template
- Turn on GitHub Pages
- Upload Objects
  -  Commit changes
- Upload Metadata
  -  Commit changes
- Configure site-wide settings using _config.yml
  -  Commit changes
- Create an Issue

6. Wrap-up
- Questions?
- Discuss homework (Olivia)
  -  Introduce how homework instructions are laid out
  -  Build a collection using your own data (run into trouble? Send us your questions as well as a link to your repository)
  -  Create an issue in the dhsi-demo repository introducing yourself and your collection
- Office hours!

7. Demo data:
- Psychiana Collection Demo Data
  -  Metadata: [https://docs.google.com/spreadsheets/d/1x48Te3duPAxh53foEihQVKTfCKUjaCCbH7TrMMd_yU4/edit?usp=sharing](https://docs.google.com/spreadsheets/d/1x48Te3duPAxh53foEihQVKTfCKUjaCCbH7TrMMd_yU4/edit?usp=sharing) 
  -  Objects: [http://lib.uidaho.edu/collectionbuilder/demo-objects.zip](http://lib.uidaho.edu/collectionbuilder/demo-objects.zip) 
- Carleton Watkins Mine Collection Demo Data
  -  Metadata: [https://docs.google.com/spreadsheets/d/1mThECwBYaUdvUrSbc9d2wbjedpYyvVD89jJ15R-7Qmo/edit?usp=sharing](https://docs.google.com/spreadsheets/d/1mThECwBYaUdvUrSbc9d2wbjedpYyvVD89jJ15R-7Qmo/edit?usp=sharing)
  - . Objects: [http://lib.uidaho.edu/collectionbuilder/watkins.zip](http://lib.uidaho.edu/collectionbuilder/watkins.zip) 

### Homework

**Create a collection using the objects you’ve prepared**

1. Create a *new* CollectionBuilder-GH collection repository using the green "Use this template" button from the CollectionBuilder-GH repository ([https://github.com/CollectionBuilder/collectionbuilder-gh](https://github.com/CollectionBuilder/collectionbuilder-gh))
-  Follow the "Generate from Template" documentation: [https://collectionbuilder.github.io/cb-docs/docs/repository/create/](https://collectionbuilder.github.io/cb-docs/docs/repository/create/) 

2. Create your collection’s metadata according to the metadata guidelines: [https://collectionbuilder.github.io/cb-docs/docs/metadata/gh_metadata/](https://collectionbuilder.github.io/cb-docs/docs/metadata/gh_metadata/) 
-  Use the CollectionBuilder-GH metadata template: [https://docs.google.com/spreadsheets/d/1Uv9ytll0hysMOH1j-VL1lZx6PWvc1zf3L35sK_4IuzI/edit?usp=sharing](https://docs.google.com/spreadsheets/d/1Uv9ytll0hysMOH1j-VL1lZx6PWvc1zf3L35sK_4IuzI/edit?usp=sharing) 
-  Be sure that you’ve included the required fields, and that filenames and file extensions in your metadata match the filenames and file extensions of your objects--filename is case sensitive!

3. Upload your metadata to your repository: [https://collectionbuilder.github.io/cb-docs/docs/metadata/uploading/](https://collectionbuilder.github.io/cb-docs/docs/metadata/uploading/) 

4. Add your prepared objects to the objects folder in your repository: [https://collectionbuilder.github.io/cb-docs/docs/objects/gh-objects/](https://collectionbuilder.github.io/cb-docs/docs/objects/gh-objects/) 

5. Turn on GitHub Pages: [https://collectionbuilder.github.io/cb-docs/docs/deploy/gh-pages/](https://collectionbuilder.github.io/cb-docs/docs/deploy/gh-pages/) 

6. Adjust site-wide settings in the "_config.yml" file: [https://collectionbuilder.github.io/cb-docs/docs/config/](https://collectionbuilder.github.io/cb-docs/docs/config/) 

7. Create an issue on the dhsi-demo repository ([https://github.com/CollectionBuilder/dhsi-demo/issues](https://github.com/CollectionBuilder/dhsi-demo/issues)) that:
-  Describes your collection, and;
-  Includes links to your collection repository and live collection site.

8. Ensure software is set up on your personal computer (you’ve likely already done this by now)! [https://collectionbuilder.github.io/cb-docs/docs/software/](https://collectionbuilder.github.io/cb-docs/docs/software/) 
-  Git 
-  Text editor
-  Ruby
-  Jekyll + Bundler

9. Get in touch if you run into any issues or have any questions!

----------------------------------------------------------------------------------------------------------------------------------------------

## Day 2: Tuesday, June 8

**Topics**: Git, Git Clone, Local Development with Jekyll, YML, CSV

### Major Learning Objectives: 

**Conceptual** 
- Understand the differences between Git, GitHub, GitHub Pages, and GitHub Desktop
- Understand the difference between Ruby and Jekyll
- Understand how and why one would develop locally and collaborate via the cloud*

**Technical** 
- Be able to start a development server on your computer
- Be able to locate your project repository and edit your repository files on your computer
- Be able to perform the basic Git workflow (commit, push, pull) locally and check results on GitHub + GitHub Pages*

### Day 2 Workshop Recording:

[https://youtu.be/pZz5LYwdLUA](https://youtu.be/pZz5LYwdLUA)

### Day 2 Outline:

1. Quick check in (look at Issue introductions)

2. CollectionBuilder technical overview - [slides](https://docs.google.com/presentation/d/1Wqk1Qw05afekTWMyfPEX3WST-J-16TyP6Ea5BPZWjV8/edit?usp=sharing) (Evan)
-  Define Git, GitHub, GitHub Pages, Jekyll, Ruby, Bundler, CollectionBuilder 

3. Software setup check in (Devin)
-  If you're having problems, we will help you! (after class)

4. [From Clone To Push: A CollectionBuilder + GitHub Desktop Step by Step](https://docs.google.com/document/d/16sGhq_FEzwdiBzpMRW0m4VuBzbthLY8uG9gCFhwg1aY/edit?usp=sharing) (Devin)
-  Introduction to Git
  -  Clone your homework collection to your computer using GitHub Desktop
-  Introduce the local development environment:
  -  Folder of files = CollectionBuilder project
  -  Text editor: Visual Studio Code
  -  Command Line Jekyll (bundler best practices/troubleshooting)
-  Use Jekyll to serve your site locally
  -  Quick intro to _data/theme.yml (much more later!) and _config.yml
  -  Edit files locally 
-  Introduce Git commit, push, and pull from your computer using GitHub Desktop
-  Check your GitHub pages site to see changes go "Live"

5. Overview of Git pull, commit, and push using the command line and Visual Studio Code (alternate methods to GitHub Desktop) (Evan)

6. Further customize collection locally and push (if time allows) (Olivia)
-  _data/theme.yml
  -  Default page settings 
-  _data/config .csv
  -  Customize page settings (Browse, Nav, Metadata)

### Homework 

*Pull your collection down to your computer and customize your collection*

1. Clone your collection repository: [https://collectionbuilder.github.io/cb-docs/docs/repository/clone/](https://collectionbuilder.github.io/cb-docs/docs/repository/clone/) 
-  Depending on your preferences:
  -  Clone using GitHub Desktop ([https://collectionbuilder.github.io/cb-docs/docs/repository/clone/#clone-with-github-desktop](https://collectionbuilder.github.io/cb-docs/docs/repository/clone/#clone-with-github-desktop)), (see also: [From Clone To Push: A CollectionBuilder + GitHub Desktop Step by Step](https://docs.google.com/document/d/16sGhq_FEzwdiBzpMRW0m4VuBzbthLY8uG9gCFhwg1aY/edit?usp=sharing)), or
  -  Clone using the command line ([https://collectionbuilder.github.io/cb-docs/docs/repository/clone/#clone-on-command-line](https://collectionbuilder.github.io/cb-docs/docs/repository/clone/#clone-on-command-line)) 

2. Open your collection repository in Visual Studio Code: [https://collectionbuilder.github.io/cb-docs/docs/repository/open/](https://collectionbuilder.github.io/cb-docs/docs/repository/open/) 

3. Serve your collection locally on your Jekyll development server: [https://collectionbuilder.github.io/cb-docs/docs/repository/generate/](https://collectionbuilder.github.io/cb-docs/docs/repository/generate/)
-  "bundle install" (first time only): [https://collectionbuilder.github.io/cb-docs/docs/repository/generate/#bundle-install-1st-time-only](https://collectionbuilder.github.io/cb-docs/docs/repository/generate/#bundle-install-1st-time-only)
-  "bundle exec jekyll s": [https://collectionbuilder.github.io/cb-docs/docs/repository/generate/#jekyll-serve](https://collectionbuilder.github.io/cb-docs/docs/repository/generate/#jekyll-serve) 

4. Edit some files in your repository. 
-  Practice editing the default page settings by adding values to variables in the _data/theme.yml file: [https://collectionbuilder.github.io/cb-docs/docs/theme/](https://collectionbuilder.github.io/cb-docs/docs/theme/)
-  Customize your site using the config CSVs in the _data folder: [https://collectionbuilder.github.io/cb-docs/docs/customization/](https://collectionbuilder.github.io/cb-docs/docs/customization/)

5. Use Git to commit and push changes to your repository
-  Select the method that works best for you:
  -  Commit and push with GitHub Desktop: [https://collectionbuilder.github.io/cb-docs/docs/repository/commit/#commit--push-with-github-desktop](https://collectionbuilder.github.io/cb-docs/docs/repository/commit/#commit--push-with-github-desktop)
  -  Commit and push with Visual Studio Code: [https://collectionbuilder.github.io/cb-docs/docs/repository/commit/#commit--push-on-vs-code](https://collectionbuilder.github.io/cb-docs/docs/repository/commit/#commit--push-on-vs-code))
  -  Commit and push with the command line: [https://collectionbuilder.github.io/cb-docs/docs/repository/commit/#commit--push-on-command-line](https://collectionbuilder.github.io/cb-docs/docs/repository/commit/#commit--push-on-command-line) 

6. Get in touch if you run into any issues or have any questions!

----------------------------------------------------------------------------------------------------------------------------------------------

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

----------------------------------------------------------------------------------------------------------------------------------------------

## Day 4: Thursday, June 10

**Topics**: Jekyll, Liquid, JavaScript, JSON, Markdown

### Major Learning Objectives: 

**Conceptual** 
- Understand how Jekyll creates pages and site architecture using permalinks and layouts
- Understand how Jekyll uses the Liquid programming language to populate CollectionBuilder layouts
- Understand the difference between #collectionsasdata and collections in context*

**Technical** 
- Be able to use _data/theme.yml to customize the look of your project
- Be able to recognize Liquid within a Jekyll project
- Be able to locate an Include file within the repository
- Be able to find the data assets and manipulate them
- Be able to create a new page in the project*

### Day 4 Workshop Recording:

[https://youtu.be/IclcqkS82fg](https://youtu.be/IclcqkS82fg)

### Day 4 Outline:

1. Follow up on About pages and interpretive assignment (Evan)
-  Does everyone understand how the includes work? Where to find them? 
-  Notes about Bundler Gemfile and Gemfile.lock

2. What is a Jekyll/CollectionBuilder web page? (Olivia)
-  Create a new Cloud page
  -  Frontmatter power
-  Expose your new pages in the Navigation Menu 
  -  add a dropdown to the config-nav.csv
-  Create a TimelineJS page 
  -  Where is the data? How is it being created/transformed/consumed? 

3. How to build and deploy your site (Evan)
-  Jekyll build vs. jekyll serve
-  Deploying outside of GitHub Page - objects and web site
-  CollectionBuilder Types --> CSV
-  Demonstrate CSV rake generate derivatives 
- Demonstrate moving files to server

4. Explore possibilities for expanding and combining digital scholarship projects using static web style of development (Devin)
- [Tool, Template, Service, Infrastructure](https://docs.google.com/presentation/d/1Arp1NEZ37ppRyXJdjlYdf43tuHsQgnpc6Ih1-fhocEk/edit?usp=sharing) 
- Look at highly customized CollectionBuilder instances and related projects

### Homework

**Polish collections, complete some readings on static web + DH, brainstorm your potential future uses of CollectionBuilder** 

1. Polish and finish up work on your collections in preparation for show and tell tomorrow. 
-  Follow the documentation if you’d like to implement any of the advanced changes demonstrated in today’s class:
  -  Repurpose the timeline: [https://collectionbuilder.github.io/cb-docs/docs/advanced/repurposetimeline/](https://collectionbuilder.github.io/cb-docs/docs/advanced/repurposetimeline/) 
  -  Create a new TimelineJS page: [https://collectionbuilder.github.io/cb-docs/docs/advanced/timelinejs/#creating-a-new-timeline-page--nav-dropdown](https://collectionbuilder.github.io/cb-docs/docs/advanced/timelinejs/#creating-a-new-timeline-page--nav-dropdown)
  -  Create a new Cloud page: [https://collectionbuilder.github.io/cb-docs/docs/advanced/cloudpage/](https://collectionbuilder.github.io/cb-docs/docs/advanced/cloudpage/) 
  -  Add a dropdown to the Navigation Menu: [https://collectionbuilder.github.io/cb-docs/docs/customization/config-nav/#dropdown_parent](https://collectionbuilder.github.io/cb-docs/docs/customization/config-nav/#dropdown_parent) 

2. Read the following articles in preparation for tomorrow’s class:
-  Gil, Alex. "The User, the Learner, and the Machines We Make." *Minimal Computing*, May 21, 2015, [https://go-dh.github.io/mincomp/thoughts/2015/05/21/user-vs-learner/](https://go-dh.github.io/mincomp/thoughts/2015/05/21/user-vs-learner/) 
-  Wikle, Olivia, Evan Williamson, and Devin Becker. "What is Static Web and What’s it Doing in the Digital Humanities Classroom?" *dh+lib*, Special Issue: Literacies in a Digital Humanities Context, 2020, [https://dhandlib.org/2020/06/22/what-is-static-web-and-whats-it-doing-in-the-digital-humanities-classroom/](https://dhandlib.org/2020/06/22/what-is-static-web-and-whats-it-doing-in-the-digital-humanities-classroom/) 

3. Brainstorm some ways you might use CollectionBuilder in your unique context.

----------------------------------------------------------------------------------------------------------------------------------------------

## Day 5: Friday, June 11

**Topics**: Static Web, DH

### Day 5 Workshop Recording:

[https://youtu.be/9KOakajfydQ](https://youtu.be/9KOakajfydQ)

### Day 5 Outline:

1. Static web discussion - [slides](https://docs.google.com/presentation/d/1EXWqdF0P74T8-zW5CYTvLuv6v6z-6ITF4Js824clPVU/edit?usp=sharing) (Olivia)
-  [Lib-Static](https://lib-static.github.io/) (static web tools in libraries)
-  Possibilities of the Lib-Static philosophy
  -  Look at [Ed](https://minicomp.github.io/ed/), [Wax](https://minicomp.github.io/wax/), and [Oral History as Data](https://uidaholib.github.io/oral-history-as-data/)
  -  What code or concepts might you want to "steal" for your own projects? (“Good digital humanists steal!” —Devin)

2. Show and Tell!
-  Showcase the collection(s) you’ve created during this course

3. Wrap up 
-  Concerns, questions, or feedback?

# CollectionBuilder Resources

## CollectionBuilder, Customized

"[Civilian Conservation Corps in Idaho](https://www.lib.uidaho.edu/digital/cccidaho/)" is a project in collaboration with U of I history faculty who wished to share materials accumulated during archival research. This enables an opportunity to go beyond the final publication, providing access to a unique curated collection.

"[1918 Flu Pandemic Collection](https://www.lib.uidaho.edu/digital/1918flu/)" is a special exhibit created by Special Collections staff to highlight timely, thematic content. The agility and simplicity of CollectionBuilder allows staff to learn how to contribute ideas, content, and long form writing to efficiently collaborate with digital librarians to bring this type of collection to life. We would not have been able to publish this sort of collection using our traditional repository workflow.

"[Historic Japanese Ceramic Comparative Collection](https://www.lib.uidaho.edu/digital/hjccc/)" is an early customized version of a CollectionBuilder-SA template developed in collaboration with a graduate student in Archeology to publish her unique research beyond a dissertation. This highlights the project’s flexibility to adapt to different content types and means of navigation. The graduate student was able to meaningfully contribute to the collection site by creating data and content, without needing skills in web development.

"[University of Idaho: Then and Now](https://www.lib.uidaho.edu/digital/campushistory/)" is a project created by an undergraduate student during a fellowship with the Center for Digital Inquiry and Learning. The student explored archival images of campus, then rephotographed the locations to provide “then & now” comparisons. This shows how the CollectionBuilder template can be quickly modified and extended with new features, such as KnightLab JuxtaposeJS. 

"[Mining History in Idaho](https://uidaholib.github.io/hist404-fall2018/)" is a student-led collection created by an undergraduate history course using an early version of CollectionBuilder-GH. Creating the collection provided students an experience in archival research, digitization, metadata creation, and web publishing.

"[Adult Salmon and Steelhead Migration Studies: 1996-2014](https://www.lib.uidaho.edu/digital/ferl/)" is an early stand alone collection built from metadata and PDFs submitted by an ecology lab to preserve research for long term open access. This highlights the possibilities to provide flexible institutional repository services that represent the unique contexts of research that might otherwise never be published online.

## Websites and Repositories 

* CollectionBuilder main site (info and documentation), [https://collectionbuilder.github.io/](https://collectionbuilder.github.io/)

* CollectionBuilder GitHub organization (code repositories), [https://github.com/collectionbuilder/](https://github.com/collectionbuilder/)

* CollectionBuilder presentations repository, [https://osf.io/5sevc/](https://osf.io/5sevc/)

* University of Idaho Digital Collections (mostly CollectionBuilder-based), [https://www.lib.uidaho.edu/digital/collections.html](https://www.lib.uidaho.edu/digital/collections.html)

* Center for Digital Inquiry and Learning (University of Idaho digital scholarship unit, following mostly Lib-STATIC style development), [https://cdil.lib.uidaho.edu/](https://cdil.lib.uidaho.edu/) 

## CollectionBuilder Types 

There are different versions or "types" of CollectionBuilder template depending on where you want to store the collection objects, your technical expertise, and the aims of your project. There are currently three main versions:

* [CollectionBuilder-GH](https://github.com/CollectionBuilder/collectionbuilder-gh) ("GitHub Pages") - a simplified template designed for free hosting on GitHub Pages that can be implemented without installing anything on your computer. It is intended as a pedagogical tool useful for classroom projects, teaching about digital libraries, or getting started with CollectionBuilder. 

* [CollectionBuilder-CONTENTdm](https://github.com/CollectionBuilder/collectionbuilder-contentdm) ("Skin") - a template to create a new front end on top of existing CONTENTdm digital collections to provide a better user interface for browsing and discovery. It uses APIs to call images into the web pages from your existing repository. 

* [CollectionBuilder-SA](https://github.com/CollectionBuilder/collectionbuilder-sa) ("Stand Alone") - a fully featured template designed for self hosting, where there is a bit more you will need to set up on your own, but provides a powerful, self contained package ready to flexibly build new digital projects.

Additionally, a complete digital library replacement with an ElasticSearch component providing central indexing is in a prototype stage under active development.

## CollectionBuilder Basics

CollectionBuilder is a set of flexible open source templates for creating digital collection and exhibit websites that are driven by metadata and powered by modern static web technology. To generate a digital collection website, users:

* Create metadata in a spreadsheet

* Organize a corresponding folder of digital objects (images, PDFs, videos, etc)

* Make a copy of the CollectionBuilder template code 

* Configure and customize the site using built-in options

* Write contextual content in Markdown

Once set up, the CollectionBuilder project is transformed by the popular static site generator [Jekyll](https://jekyllrb.com/) (installed on a laptop or used through an automatic build process such as GitHub Pages hosting service) into a complete website for browsing and contextualizing the collection. The output is static HTML that can be copied to any basic web server, or hosted for free on GitHub Pages, providing a simple, preformant, and secure website—alongside clean data and metadata ready for long term digital preservation.

![image alt text](image_0.png)

CollectionBuilder templates are a packaged folder of plain text files, including modular chunks of HTML, CSS, and JS, and helpful development libraries such as Bootstrap. Users need not know anything about Jekyll, Liquid, or the other tools that power CollectionBuilder to get started. Instead, they begin by focusing on their collection’s metadata and digital objects independent of the system, then follow step-by-step documentation to add them to the project template. 

The CollectionBuilder code consumes the collection metadata added by the user to automatically generate browsing features, items pages, data derivatives, and rich SEO markup. Metadata drives the core of the user interface, creating interactive browsing pathways and visualizations that encourage visitors to explore and discover content while also representing overall context, transforming high quality description into a rewarding user experience.

![image alt text](image_1.png)

## CollectionBuilder Workflow

To demonstrate how CollectionBuilder works, this section walks through our current pedagogical version, CollectionBuilder-GH, a tool intended as a simple template for hands-on teaching about digital libraries. 

CollectionBuilder-GH can be used in a workshop or classroom setting to take participants through digitization and metadata creation, to having a live digital collection website hosted on GitHub Pages without installing any software (this contrasts with the other CollectionBuilder versions which rely on [Jekyll](https://jekyllrb.com/) being installed on a local development machine). The only requirement for both instructor and participants is a GitHub account and a web browser. Similar learning experiences often use [Omeka](https://omeka.org/) or other DAMS/[CMS](https://en.wikipedia.org/wiki/Content_management_system) platforms with extensive infrastructure requirements that are overkill for one-off projects. Although these platforms feature familiar GUI administration interfaces, they are not necessarily simple to learn and customize. CollectionBuilder-GH aims to be well documented and easy to configure by following the example—if you match the metadata template, a fully functional website will be automatically generated. Customization is learned in additional small steps, encouraging scaffolded learning about web and data fundamentals. A project in "minimal computing", CollectionBuilder-GH provides a depth of learning opportunities, allowing users to take complete ownership over the project while making their work open to the world. 

1. Setup: After getting set up with GitHub accounts and orientation, users start their new project by creating a copy of the code on GitHub by clicking the "Use this Template" button, [https://github.com/CollectionBuilder/collectionbuilder-gh](https://github.com/CollectionBuilder/collectionbuilder-gh) 

2. Prepare Objects: Users then prepare their folder of digitized objects (generally images and/or PDFs) following the documented standards, and upload them into their project repository’s "objects" directory. This is an opportunity to teach data skills such as file naming, preservation formats, and media editing.

3. Prepare Metadata: Users prepare a spreadsheet of metadata for the objects, following the CollectionBuilder metadata template (which is based on digital libraries best practices and standards). We typically use Google Sheets, allowing easy collaboration with groups of participants. This hands-on digitization and metadata creation experience helps reveal the real labor and decision-making processes that go into the creation of digital library data. Skills learned manipulating media files and working with spreadsheets are more transferable data fundamentals than comparable workflows in CMS interfaces which focus on forms and clicks. Once the metadata is prepared, it is downloaded/exported as a CSV, and uploaded into their project repository’s  "_data" directory.

4. Configure Site: With the well-structured data prepared, users can begin working on the website configuration, including the "_config.yml" which provides the base settings for Jekyll websites, such as site “title,” “tagline,” and “description.” Config files can be edited using GitHub’s web interface. 


5. Add Descriptive Content: Users can edit content pages, such as the About page, to provide context for their collection. Page content is styled using [Markdown](https://guides.github.com/features/mastering-markdown/), providing an easy to learn and write markup language. 

6. Activate GitHub Pages: With the click of a button, users can activate GitHub’s free hosting service and have a live website in seconds. In the background, the platform automatically runs the static site generator (Jekyll) over the source code, outputs a complete website (HTML, CSS, JSON, and JS files), and serves it up to the world. Users navigate to their site to discover their new digital collection and explore the visualizations. They will likely discover interesting metadata anomalies that were not apparent when working on the spreadsheet—a teachable moment about how to debug your project!

By creating a collection using CollectionBuilder, students develop interwoven technical and critical skills, including fundamental data literacies related to controlled vocabularies, unique identifiers, and descriptive practice. These lessons are reinforced when their metadata is transformed into a digital collection on the web, inevitably surfacing anomalies, breakages, and misrepresentations tied to issues in the metadata that they return to the spreadsheet to fix. Small "next steps" invite students to start learning more about the templates generating the website, encouraging incremental development of further web skills.

Outside of the classroom or workshop setting, we still see CollectionBuilder as a tool rooted in learning. CollectionBuilder is unlike common Content Management Systems (CMS) or Digital Asset Management (DAM) platforms that most institutions use—it is not a visual GUI tool and there is no admin interface, which can intimidate and contribute to an initial learning curve. However, it is designed to be 'do-able' and accessible for librarians and digital humanities practitioners—and once understood, users will be rewarded with a flexible and sustainable template for creating digital collections, as well as data and web skills transferable to any digital project. This opportunity for professional development provides unique agency for librarians to take full control over their systems and pursue new initiatives and ideas equipped with CollectionBuilder components as a recipe book of solutions.

Using other versions of CollectionBuilder follows a similar workflow as described above, but allows for further customization, features, and optimization of the site. Users edit the template code on their own computers and run Jekyll to provide a local development server to test their work. The code aims to be modular, understandable, and well-documented with the goal to be sustainable for a low-resourced digital libraries team. Once a collection is ready to deploy, the developer uses Jekyll to build the self-contained static website and copies the files over to a basic web server or hosting service.

## The Lib-STATIC Methodology

Since around 2015 static site generators and the "[JAMstack](https://jamstack.org/what-is-jamstack/)" approach have exploded in the web development landscape—utilizing simplified markup, plain text data files, and web APIs to create complete websites without the need for complex server applications, databases, or content management systems. Rather than relying on server-side processing to generate a dynamic page on the fly for each user request, static web tools “pre-render” every page into HTML, CSS, and JS files that can be delivered directly to users with speed, efficiency, and security from the most basic web servers or services. This modern static web approach provides high performance for users, minimal infrastructure requirements for IT, and lower barriers for developers. 

Eager to explore this potential in the library context, faculty librarians at the University of Idaho (U of I) have been developing digital collections, digital humanities projects, and instructional content using static web tools for more than five years. Informed by the philosophy of [minimal computing](https://go-dh.github.io/mincomp/about/), they have been documenting the "Lib-STATIC" methodology to begin building a community of practice centering digital infrastructure approaches around the unique needs, values, and opportunities of libraries. 

The primary principles of the methodology are summarized in the visualization below:

![image alt text](image_2.png)

Simply stated, Lib-STATIC-inspired tools seek to apply the techniques of the modern static web approach to pragmatically solve problems in the digital library ecosystem. It differs greatly from the predominant model for platform and tool building for academic libraries as it does not require complex infrastructure nor extensive IT staffing (or third party vendors) to implement and maintain the systems put into use. Instead, the Lib-STATIC approach focuses on practical, sustainable workflows using data-driven static web templates hosted on simplified infrastructure while leveraging the in-house specialized skills of librarians in metadata, data, and organization. This provides librarians unique agency and ownership over their systems, as well as meaningful opportunities for professional development leading to fundamental digital skills (instead of the "[buttonology](https://crln.acrl.org/index.php/crlnews/article/view/16833/18427)" of a single platform). The focus on clean data and simple systems enables a more agile and responsive approach, allowing the iterative development of features, gradual acquisition of developer skills, and flexible migration between hosts without the need for deep investment.

Lib-STATIC acknowledges that all digital projects require investment in learning and seeks to maximize the local impact and value of learning during the process, while establishing technical solutions and social workflows that more closely match the structure of academic work cycles and needs. The simplified infrastructure and development environment of static web approaches are uniquely suited to enable:

* Periods of focused development and collaboration, followed by much longer periods of minimal maintenance.

* Project work focused on creating data independent of platform, which simplifies the initial infrastructure decision points and overhead while ensuring preservation- and migration-ready content.

* Rapid design and data iterations—building projects in smaller steps allows data to be published faster, getting feedback earlier with less initial investment yet future opportunity for phases of progressive enhancement.

* A focus on modular components, templates, and recipes that encourage learning investment on one project leading to efficiencies on another, building complementary work that powers further research and learning.

* Public documentation and sharing, making investment more reusable while creating artifacts of learning alongside research and publications.

The Lib-STATIC methodology has grown out of U of I librarians’ experience collaborating with faculty, students, staff, and other organizations to create digital collection, digital scholarship, and teaching projects. Bogged down in the process of standing up and maintaining heavy infrastructure platforms for one off projects, they found a real need for a more flexible and sustainable approach to creating websites. The static web approach has freed up energy and time to pursue new initiatives and ideas, leading to unique collaborations and learning opportunities. Projects have included an [open music text book](https://intmus.github.io/), [workshop outlines](https://evanwill.github.io/go-go-ghpages-b/), [interpretive oral history projects](https://ctrl-shift.org/), a [scholarly translation edition](https://thecdil.github.io/mancini_source/), [scientific research archives](https://www.lib.uidaho.edu/digital/ferl/), [classroom digitization experiences](https://uidaholib.github.io/hist404-fall2018/), [community digital collections](https://www.lib.uidaho.edu/digital/lcheritage/), [Special Collections exhibits](https://www.lib.uidaho.edu/digital/1918flu/), and the main [library website](https://www.lib.uidaho.edu/)--the Lib-STATIC methodology has truly infused our work! Each collaboration has advanced new solutions, features, and concepts which have in turn contributed to the development of several refined templates designed as reusable tools or bases for adaption, including [Oral History as Data](https://github.com/uidaholib/oral-history-as-data) and CollectionBuilder. 

# Readings

Becker, Devin, Evan Williamson, and Olivia Wikle. "CollectionBuilder-CONTENTdm: Developing a Static Web ‘Skin’ for CONTENTdm-based Digital Collections,"* Code4Lib Journal* 49, 2020, [https://journal.code4lib.org/articles/15326](https://journal.code4lib.org/articles/15326) 

Dombrowski, Quinn. "Sorry for all the Drupal: Reflections on the 3rd anniversary of ‘Drupal for Humanists,’"* Quinn Dombrowski* (blog), November 8, 2019, [http://www.quinndombrowski.com/?q=blog/2019/11/08/sorry-all-drupal-reflections-3rd-anniversary-drupal-humanists](http://www.quinndombrowski.com/?q=blog/2019/11/08/sorry-all-drupal-reflections-3rd-anniversary-drupal-humanists) 

Gil, Alex. "The User, the Learner, and the Machines We Make." *Minimal Computing*, May 21, 2015, [https://go-dh.github.io/mincomp/thoughts/2015/05/21/user-vs-learner/](https://go-dh.github.io/mincomp/thoughts/2015/05/21/user-vs-learner/) 

Nowviskie, Bethany. "speculative collections." *Bethany Nowviskie* (blog), October 27, 2016, [http://nowviskie.org/2016/speculative-collections/](http://nowviskie.org/2016/speculative-collections/). 

Russell, John E., and Merinda Kaye Hensley. "Beyond buttonology," *College & Research Libraries News*, 2017, [https://crln.acrl.org/index.php/crlnews/article/view/16833/18427](https://crln.acrl.org/index.php/crlnews/article/view/16833/18427) 

Varner, Stewart. "Minimal Computing in Libraries: Introduction." *Minimal Computing*, January 25, 2017, [https://go-dh.github.io/mincomp/thoughts/2017/01/15/mincomp-libraries-intro/](https://go-dh.github.io/mincomp/thoughts/2017/01/15/mincomp-libraries-intro/)

Visconti, Amanda. "Introducing Static Sites for Digital Humanities Projects (why & what are Jekyll, GitHub, etc.?)," *Literature Geek*, December 8, 2015, [http://literaturegeek.com/2015/12/08/WhyJekyllGitHub](http://literaturegeek.com/2015/12/08/WhyJekyllGitHub) 

Wikle, Olivia, Evan Williamson, and Devin Becker. "What is Static Web and What’s it Doing in the Digital Humanities Classroom?" *dh+lib*, Special Issue: Literacies in a Digital Humanities Context, 2020, [https://dhandlib.org/2020/06/22/what-is-static-web-and-whats-it-doing-in-the-digital-humanities-classroom/](https://dhandlib.org/2020/06/22/what-is-static-web-and-whats-it-doing-in-the-digital-humanities-classroom/) 

Williamson, Evan, Olivia Wikle, Devin Becker, Marco Seiferle-Valencia, Jylisa Doney, and Jessica Martinez, "Using Static Web Technologies and Git-based Workflows to Re-Design and Maintain a Library Website (Quickly) with Non-Technical Staff." College & Undergraduate Libraries, 2021, (PDF included in this packet)

