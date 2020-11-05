# CollectionBuilder

> This repository hosts the home page and documentation site for the CollectionBuilder project,
> <https://collectionbuilder.github.io/>

CollectionBuilder is a lightweight, flexible tool for creating digital collection and exhibit websites driven by metadata, and powered by modern static web technology.

![collectionbuilder icon](images/collectionbuilder2.png)

The user provides a well structured metadata spreadsheet and a directory of digital files, that CollectionBuilder will process to generate a variety of visualizations--surfacing the unique facets and features of the content, creating interactive pathways to browse and discover items while providing overall context. 
Each visualization is configurable using a few basic variables or config files. 
Each is a self contained static web page that can be hosted on the most basic web servers without the need for a database or server-side processing language, enabling simple security and speedy performance. 

At it's heart, CollectionBuilder is a set of Jekyll projects or templates designed following the [Lib-STATIC](https://lib-static.github.io/) development methodology which aims to lower the barriers for development and deployment of digital collections, while upholding the unique values and perspectives of [GLAM institutions](https://en.wikipedia.org/wiki/GLAM_(industry_sector)). 
CollectionBuilder prioritizes pragmatic, sustainable, and simplified approaches to infrastructure to ensure the tool is "do-able" and approachable for digital knowledge workers in libraries and museums, empowering them to take control of their web systems.
An experiment in "minimal computing", CollectionBuilder provides a depth of learning opportunities and development possibilities, allowing users to take complete ownership over the project and make their work open to the world.

## Concept 

The growing maturity of static generators such as Jekyll, offer a robust and viable alternative to traditional content management systems for creating efficient and secure websites requiring a fraction of the server overhead, while allowing a more flexible and unique front end.
Thus, CollectionBuilder shifts energy away from clicking buttons on heavy DAMS platform interfaces, and back on creating the clean, polished metadata and objects fundamental to digital libraries--building collections as data.

This shift to focusing on clean data and simple systems enables a more agile and responsive approach, allowing iterative development of features, gradual acquisition of developer skills, and flexible migration between hosts without the need for deep investment. 
There will still be learning curves and frustration, to be sure, but by removing some of the overwrought features and extensive infrastructure requirements of library systems currently used and developed today, the Lib-STATIC methodology ensures those central library values of usability and accessibility are primary to any tool developed following its principles.

## Design

CollectionBuilder is built on top of a stack of popular, mature, and well documented web development tools including Bootstrap front-end framework and JavaScript libraries such as jQuery and Leaflet, but aims to keep dependencies simple and easy to manage.
The project consists of a template of modular HTML, SASS, JavaScript, and Ruby components which are knit together by Jekyll to generate a complete static site (i.e. a folder of HTML, CSS, JSON, and JavaScript files).
The plain text source code files are easily version controlled with Git, enabling collaboration and project management on cloud platforms such as GitHub, GitLab, or BitBucket.
Jekyll provides a local development server, simplifying iterative testing (and learning) and eliminating the need for a test server.
For public deployment, the output folder of static site assets can be copied onto a basic web server (no server-side processing or database is required), or can be served directly by free services such as GitHub Pages or GitLab Pages, that provide automatic Jekyll building and hosting.

CollectionBuilder projects are:

- Agile (investment in data and fundamental skills, rather than in heavy infrastructure, enables responsive change)
- Future-ready (simple data based system is always ready for migration to other platforms)
- Preservation-ready (organized projects which clearly separate presentation from data, provide packages ready for longterm digital preservation)

We envision CollectionBuilder being used by libraries and cultural heritage institutions in three main ways: 

1. the creation of stand-alone library digital collections and exhibits hosted on basic static web infrastructure.
2. the creation of "skins" to provide better UX and context on top of existing digital collection management systems (such as CONTENTdm).
3. as a pedagogical tool for learning about digital collection development and fundamental data and web skills. 

## Current projects

- [collectionbuilder-gh](https://github.com/CollectionBuilder/collectionbuilder-gh) - A simple template for hands-on teaching about digital libraries, designed to be hosted on GitHub Pages. It can be used in a workshop setting to take participants through digitization and metadata creation, to having a live collection site for free. An static alternative to teaching with full scale DAMS such as Omeka.
- [collectionbuilder-contentdm](https://github.com/CollectionBuilder/collectionbuilder-contentdm) - a template for creating digital collection exhibits on top of existing CONTENTdm repositories. It uses item API's to create an engaging "skin" on top of an existing digital collection repository using your existing collection metadata.

If you are interested in using CollectionBuilder, or are already using it, please drop us a line (libstatic.uidaho@gmail.com) since we would love to learn more about it's use in the wild. 
There are also currently opportunities to collaborate on CollectionBuilder.

## License

CollectionBuilder documentation and general web content is licensed [Creative Commons Attribution-ShareAlike 4.0 International](http://creativecommons.org/licenses/by-sa/4.0/). 
This license does *NOT* include any objects or images used in digital collections, which may have individually applied licenses described by a "rights" field.
CollectionBuilder code is licensed [MIT](https://github.com/CollectionBuilder/collectionbuilder.github.io/blob/master/LICENSE). 
This license does not include external dependencies included in the `assets` directory, which are covered by their individual licenses.
