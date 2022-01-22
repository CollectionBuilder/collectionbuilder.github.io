---
title: General
sectionid: general
section_order: 1
---

## What is CollectionBuilder?

{:.my-4}
CollectionBuilder is a set of flexible, static web [templates]({{ '/templates.html' | relative_url }}) for creating digital collection websites. These templates  are driven by metadata and powered by modern static web technology. Using three primary components—a spreadsheet of metadata, a directory of assets, and a configuration file—CollectionBuilder helps users to build and customize sustainable, digital collections and exhibits for free, learning valuable development practices in the process.  

## How does it work?

CollectionBuilder uses the static site generator Jekyll, together with some particular workflows, to help users generate digital collections and exhibits from their own spreadsheets and digital media. 

Each CollectionBuilder template exists as a repository on GitHub that users are asked to copy and modify by replacing the default values, metadata spreadsheet, and digital objects with their own. Once replaced, CollectionBuilder iterates over a user's data to create a series of static HTML, CSS, and JavaScript files that can be served from any web server. With these customized files, CollectionBuilder builds maps, timelines, word clouds, and other visualizations, as well as browsing features, item pages, and new, reusable data formats that can be downloaded by users and processed/indexed by machines.

## How Can I Use It?

We have [extensive documentation](https://collectionbuilder.github.io/cb-docs/) to get you started. In short: 
- Choose a template that matches your project goals. 
- Go to that template's GitHub repository.
- Copy the template by clicking "Use This Template." 
- Upload your metadata to the _data directory 
- And then edit the _config.yml to point to that file. 

You'll need to make sure your metadata has [a few required fields](https://collectionbuilder.github.io/cb-docs/docs/metadata/), but other than that, CollectionBuilder is adaptable to a wide variety of data. 

## Who's Behind This?

CollectionBuilder is designed and maintained by librarians at the [University of Idaho](https://www.lib.uidaho.edu), following the [Lib-STATIC](https://lib-static.github.io/) approach, a methodology committed to leveraging static-web technologies and librarians' specialized skills in metadata and classification to create engaging web publications. 

The project comes out of work done at the library's digital humanities center, the [Center for Digital Inquiry and Learning](https://www.lib.uidaho.edu). 

CollectionBuilder has received support from the University of Idaho Library. From 2019-2021, we were supported by a National Leadership Grant from the Institute for Museum and Library Services (IMLS). 
