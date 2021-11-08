---
step: 0
permalink: /workshop/dhsi/introduction.html
video: 
title: Introduction
shorttitle: Intro
overview: "A brief overview of CollectionBuilder DHSI Course, with Course Description, Objectives, and some general concepts."
---

#### Creating Digital Collections with Minimal Infrastructure: Hands On With CollectionBuilder for Teaching and Exhibits.

The original coursepack can be found here: [http://bit.ly/cb-dhsi2021](http://bit.ly/cb-dhsi2021)

Location: Wherever you are!

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
