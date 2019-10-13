

## Introduce Yourself

We'd like to start the workshop by hearing who you are and where you're from. We'd also love to hear about your general experience with CONTENTdm and your digital collections. 

## Introduce Ourselves

Olivia, Communications/Assessment Director for Grant

Devin, Project Director

Evan, Technical Director

Absent: Jylisa Doney, Documentation Director

## The Tool, the Methodology, and the Grant

### Tool - CollectionBuilder

Over the course of our years designing digital collection interfaces, its become apparent that the metadata itself is the most important aspect of a digital collection. As such, we've built a tool that puts the metadata forward, and uses it to build its visualizations and browsing features. 

CollectionBuilder uses static web technologies to build digital collection and exhibit pages from metadata. The tool generates item pages and all its visualizations and browsing features from the metadata spreadsheet provided and the config and theme files detailed later in the workshop.

The tool uses 5 main components: 

1. [Jekyll](https://jekyllrb.com/) - a static website builder (i.e. NO SERVERS!!!) that builds websites from data files using the [Liquid](https://shopify.github.io/liquid/basics/introduction/) programming language (which you don't need to know, but which is easily readable and eventually usable) and [Markdown](https://en.wikipedia.org/wiki/Markdown) files for content
2. [Git/GitHub](https://github.com/) - a way to collaborate, track changes, and import pre-built services
3. [Bootstrap 4](https://getbootstrap.com/) - a CSS/Javascript Package for easier development
4. Data Files - We use [Comma Separated Values (CSV) files](https://en.wikipedia.org/wiki/Comma-separated_values) that are just simple version of a spreadsheet and text files written in [YAML (.yml)](https://en.wikipedia.org/wiki/YAML), which are basically lists formatted in a specific fashion.

#### Design Concept

CollectionBuilder builds digital collection sites that encourage investigation and discovery. Our item and visualization pages are built with connections between them so that a user can follow their own interests when exploring a digital collection.

For instance, if you were interested in seeing all the images in our Barnard Stockbridge Photography Collection pertaining to the 1910 "Big Burn" forest fire. You could browse the collection by searching for "fire" on the browse page, then, when looking at individual item pages,you could link out to 1910 on our timeline page and see the wide variety of images collected during that year by the studio. 

And perhaps that would lead one to investigate some other subject terms or to focus on a particular town via the map. The intention is to connect users and to uncover the accretive magic of cultural heritage collections. 

As you examine these collections more closely, we feel that one can get a larger sense of the collection and the era, as well as its connection to one's own area and time frame. 

### Methodology

We call the methodology we use building CollectionBuilder and tools like it, Lib-STATIC. We've created [a little website to document the ideas that inform it](libstatic.github.io). 

Basically, we believe that the systems libraries have been locked into, particularly concerning digital collections, serve neither the librarians/GLAM professionals that maintain them and prepare their content nor the collections we are trying to promote using them. 

CollectionBuilder prioritizes pragmatic, sustainable, and simplified approaches to infrastructure to ensure the tool is 'do-able' and approachable for digital knowledge workers in libraries and museums, empowering them to take control of their web systems.

### How It Works for Us

We use CollectionBuilder to build our digital collections on top of our CONTENTdm instance. To do this, we use the tool together with a Git-Based Workflow. Basically, within our own CollectionBuilder-CONTENTdm repostory, there is a "master" branch of CollectionBuilder from which we create specific branches to build our individual collections. The trajectory looks like this: 

1. Create a new branch for a collection from our master CollectionBuilder-contentdm repository
2. Export collection metadata from CONTENTdm as a .tsv file. 
2. Import the file into a Google Sheet (or other non-excel spreadsheet program).
3. Add a metadata field for "object-id" based on CONTENTdm item number and collection name
4. Save as a CSV file. 
5. Move the file into the "_data" 

### The Grant

We are currently being funded by the Institute for Museum and Library Services (IMLS) to build, document, and promote CollectionBuilder. We hope in doing so to lay out a model for building other tools that might eventually replace other systems libraries are locked into (Lib-Guides, anyone?). 

This year's grant will let us fine-tune CollectionBuilder through our own development and through the hiring of a developer (if you know of anyone, let us know!). It will also help us to develop the type of promotional materials, documentation, and other prodcuts (like this workshop) that should help us spread the word about the tool and make it easy to adopt and use. 

The grant also provides funds for us to embed ourselves into several academic libraries and/or similar institutions to set up the techonological tools and basic workflows necessary for using the tool to build digital collections more pervasively. 

***Opportunites for Collaboration***

- **Partner!** - If you, or some insitution you know, might be interested in adopting this tool more seriously, we can offer a small ($1500) subaward to supplement the additional work involved and one of us would visit your site to help get everything set up. 
- **Feedback!** - If you have thoughts on the documentation, tool, visualizations, user interactions, or any other features in the tool, please *please* **please** provide us with feedback. Our intention in doing workshops and presentations is to gather feedback on the tool so that when our year is up we have the best, most usable version of CollectionBuilder.
- **Contribute** - If you take to the static web development model and would like to provide contributions of your own to our tool, we would LOVE to work with you and incorporate any contributions you might make. We have a code of conduct in developments for contributors.

Our highest hope for this project is to enable a small army of librarians to develop the type of tools and sites that keep the GLAM professionals in control and not subservient to bloated infrastructures and/or third-party contracts. We hope by the end of this workshop you will feel drawn to help us build that community. 

