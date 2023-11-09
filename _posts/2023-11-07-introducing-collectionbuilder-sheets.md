---
layout: post
title: Introducing CollectionBuilder-Sheets
subtitle: 
author: Devin Becker
publish-date: November 7, 2023
tags: [SHEETS, tech, announcement]
short_description: SHEETS is the newest and most versatile CollectionBuilder template. Users can now build CollectionBuilder exhibits directly from a Google Sheet.
---

CollectionBuilder-Sheets (SHEETS), the latest template for CollectionBuilder, is an innovative way to streamline the process of creating CollectionBuilder exhibits. It enables users to build digital collections directly from a Google Sheet (thus the name!), making the process easier and more immediate.

{% include feature/image.html objectid="/images/blog/sheets-homepage.png" link="https://collectionbuilder.github.io/collectionbuilder-sheets/" alt="Home page for CollectionBuilder-sheets with config modal popped up" caption="Home page for CollectionBuilder-sheets with config modal popped up" target="blank" %}


SHEETS serves as both a metadata training ground for those just starting out with digital collections and a means for more advanced users to quickly preview or collaboratively build "live" collections. Whether working alone or with faculty, students, and other collaborators, SHEETS makes it simple to get a collection up and running. Just make sure you include a few [required fields](https://collectionbuilder.github.io/cb-docs/docs/metadata/gh_metadata/#required-fields-for-collectionbuilder-gh)

You can check it out for yourself by going to [our demo site](https://collectionbuilder.github.io/collectionbuilder-sheets/), where you can load some of our demo data, or test it with your own. If you'd like step-by-step instructions and short videos to guide you through the process, check out [our SHEETS 2-part Walkthrough](https://collectionbuilder.github.io/cb-docs/docs/walkthroughs/sheets-walkthrough/). 

Below, we give a brief overview of the underlying code and list some possible use cases for SHEETS.


## How SHEETS works 

SHEETS uses the javascript library [Papa Parse](https://www.papaparse.com/) to build collections via a browser's temporary storage. Papa parse parses (ha!) the CSV data it's given, whether from a Google Sheet link or a local CSV, into a JSON array that is then used to generate the content for CollectionBuilder exhibit pages. 

{% include feature/image.html objectid="/images/blog/temporary-storage-sheets.png" link="https://collectionbuilder.github.io/collectionbuilder-sheets/" alt="Screenshot of session storage for CollectionBuilder demo site featuring Psychiana demo data" caption="This shows the session storage for our CollectionBuilder demo site. You can see a detail of the first item in our Psychiana demo data" target="blank" %}

Each page is then built from the ingested-CSV-turned-JSON-data using the templates developed for CollectionBuilder. So if you want a fresh reload of the data (i.e. you made changes in Sheets and want to see the results), simply open the page in a new window!

Using session storage like this adds flexibility, but it also means that **collections built within the SHEETS demo page are temporary**! Once you close your browser, the temporary session storage goes away and so does your collection. To continually develop your collection, however, we've built two additional options:: 

- If you'd like to make a permanent collection, you'll need to clone your own repository – check out [part 2 of our SHEETS walkthrough](https://collectionbuilder.github.io/cb-docs/docs/walkthroughs/sheets-walkthrough/#sheets-walkthrough-part-2) for instructions. 
- If you'd like to share a temporary version, however, you can do so [by including the Google Sheet link in the url](https://collectionbuilder.github.io/cb-docs/docs/walkthroughs/sheets-walkthrough/#5-share-your-test-site-via-url).

For even more technical information about how this all works, see our Technical Director Evan Williamson's docs page, [How CB-SHEETS Works (Technically)](https://github.com/CollectionBuilder/collectionbuilder-sheets/blob/main/docs/csv-parsing-setup.md), which includes details about how Papa Parse ingests the data and the template uses it to populate its pages. 


## Possible Use Cases

There are two primary methods for interacting with SHEETS: 
- [**_Via our demo site_**](https://collectionbuilder.github.io/cb-docs/docs/walkthroughs/sheets-walkthrough/), you can build a collection temporarily from a google sheet published as a CSV or a CSV on your local computer. 
- However, you'll want to **[_make a clone of our template SHEETS repository_](https://collectionbuilder.github.io/cb-docs/docs/walkthroughs/sheets-walkthrough/#sheets-walkthrough-part-2)** if you want to eventually publish the site on your own, or further customize a preview site. 

The examples below are just a few of the possible ways this framework might be used; the methods they use are listed in parentheses after the title.


### Previewing Your Own Collection Quickly 

{:.my-1}
*demo site use*

- Whether you're an archivist, historian, or enthusiast, you can quickly gather some insight into your collection by publishing your metadata and previewing it on our SHEETS demo collection site. Simply enter the link to your published your Google Sheet and watch as your collection takes shape. Note that your metadata will need to include a few [required fields](https://collectionbuilder.github.io/cb-docs/docs/metadata/gh_metadata/#required-fields-for-collectionbuilder-gh) to work properly.


### Collaborative Projects 

{:.my-1}
*both methods*

- One of the standout features of SHEETS is its ability to facilitate collaboration. Once a live Google Sheet is connected to your website, multiple contributors can build the exhibit together working on that single Google Sheet while receiving quick feedback on their edits. Each contributor can add and edit metadata, descriptions, and exhibit content, ensuring that the collective effort results in a comprehensive digital exhibit.


### Teaching Tool 

{:.my-1}
*cloned repository*

- CollectionBuilder-Sheets is a valuable tool for teaching classes and individuals. Once a live site is set up and connected to a shared Google sheet, students can access, edit, and examine metadata, gaining practical experience in understanding how digital collections are built and maintained. Students can also connect individual sites of their own prior to contributing to the class exhibit, which enables them to freely experiment with their own data, learn from their mistakes, and avoid the fear of breaking something vital.

Overall, we think SHEETS adds a new versatility to the CollectionBuilder project that will reward both teaching and exhibit development. Please reach out if you have any questions, and check out our Walkthroughs if you'd like to learn more! 

And please stay tuned to our new blog for more updates and resources as we roll out this innovative tool!