---
step: 3
permalink: /workshop/dhsi/day2.html
video: pZz5LYwdLUA
title: Day 2 - Software and Conventions
shorttitle: Day 2
overview: "An overview of the software and techniques used to create CollectionBuilder sites."
---
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
