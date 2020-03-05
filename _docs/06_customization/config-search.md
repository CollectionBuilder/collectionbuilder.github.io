---
title: Search
stub: config-search
section: customize
section_order: 7
---

{:.py-4 .mt-4 #config-search}
***

## Search Configuration (config-search.csv)

{% include bootstrap/alert.md text="This section is for **GH Users Only**" color="info" %}

This CSV enables GH users to select which metadata fields they would like indexed for the collection object search powered by [Lunr.js](https://lunrjs.com/){:target="_blank" rel="noopener"}. 
The values here will determine the results that appear when the site's users search for a term or phrase using the search box on the right-hand side of the header. 
Three columns in this CSV allow you to configure your search:

- **field**: Determines the metadata field to be indexed for search
    - *Example:* `title`, `date`, `description`, etc.
- **index**: Determines whether the field is searchable. 
    - *Options:* `true`, `false`
- **display**: Determines whether the value of that metadata field is displayed in the search results.
    - *Options:* `true`, `false`
