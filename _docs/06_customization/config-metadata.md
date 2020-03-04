---
title: Metadata
stub: config-metadata
section: customize
section_order: 2
---

{:.py-4 .mt-4 #config-metadata}
***

## Metadata / Item Page Configuration (config-metadata.csv)

The most important CSV (if you're measuring by the number of pages it creates!) is the one that controls the metadata. The `config-metadata.csv` controls how an item's metadata is displayed on its web page. 

The file provides a number of options to help control the display of the item's metadata, as well as the machine-readability/SEO indexing characteristics of the code underneath the display. The fields are described below: 

- **field**: 
This variable corresponds to the field listed in the metadata for the collection. For instance, if you have a metadata field called "original-collection," you would put "original-collection" here. 
- **display_name**: This variable is how you'd like the field to be described on the item page. So, using the example above, if you'd like the field "original-collection" to appear as "Original Archival Collection" on the item page, you'd enter "Original Archival Collection" in the second column.
- **browse_link**: 
    - *Options*: `true` or leave blank. 
    - You can either enter `true` in this column, or leave it blank. This option controls whether this element will be represented as a link from the item page back to the browse page. It is most useful for those fields, like "subject," that often have multiple entries. So, for instance, if you wanted to make the subjects in your "subject" field separate out into individual links, you'd enter `true` in the fourth column of the `config-metadata.csv`  
{% include bootstrap/alert.md text="**GH Users, please note**: 'browse_link' is included in **GH's config-metadata.csv**, but **does not work yet**. This capability will be implemented for GH in the future." color="warning" %}

*The options below this point are important for making your items as machine readable as possible, which makes them more discoverable by search engines. However, they are not necessary to make the collection itself work.* 

- **dc_map**: 
    - *Options*: [DC Terms](https://www.dublincore.org/specifications/dublin-core/dcmi-terms/), written like `DC.the_term_you_choose_from_the_site_linked`
    - If you'd like to map this piece of metadata so that it will be machine readable in the code for the page, you can enter the Dublin Core metadata field you'd like it to be represented as here. So, continuing with our original example, if you'd lke to map the "original-collection" field to be read as a Dublin Core Source element, you'd enter "DC.source" in the third column.
- **schema_map**:
    - [Schema](https://schema.org/) is a standard designed to provide structured semantic markup for search engines to better understand content of web pages. Item pages have in depth Schema markup in JSON-LD format driven by the object metadata. 
    - See the [Full Schema hierarchy](https://schema.org/docs/full.html) for more detail and options. Each item page is given the basic type of `CreativeWork`, thus metadata fields can be mapped to any of the properties listed on the [CreativeWork documentation](https://schema.org/CreativeWork). Copy the exact property name, as this value will be turned into schema JSON-LD markup. 
    - *Options*: Suggested field mappings include:
        - `headline` (i.e. the title)
        - `creator`
        - `dateCreated`
        - `description`
        - `keywords`
        - `contentLocation`
        - `encodingFormat` (This corresponds to the [format](metadata#required) field of CollectionBuilder items)
        - `license` (Should only be used with a standardized rights URL)

### Example 

{:.p-4 .bg-light .mb-4}
```
field,display_name,browse_link,dc_map,schema_map
title,Title,,DC.title,headline
creator,Creator,,DC.creator,creator
date,Date Created,,DCTERMS.created,dateCreated
date-is-approximate,Approximated Date
description,Description,,DC.description,description
subject,Subjects,true,DC.subject,keywords
location,Location,true,,contentLocation
identifier,Source Identifier
type,Type,,DC.type
format,Format,,,encodingFormat
rightsstatement,,,DC.rights,license
```


**Browse Links** 

In the case of this example, only the location and subject fields have a value (`true`) for "browse-link", so those fields will turn each indivdual subject and location term (delimited by semi-colon in that field) into a link (e.g. browse.html#dogs) that links back to a browse page view that will only list those items that share that term. 

**Dublin Core and Schema Markup** 

The title, creator, date, description, subject, and type fields in the above example all have a `dc_map` variable, so each of them would  be represented in the item page's <head> meta section in a way that follows the Dublin Core schema to enable better machine readability and indexing.

Similarly, the title, creator, date, description, subject, location, format, and rightstatement fields all have a `schema_map` entry, so each of these would be represented in an item page's <head> meta section in a way that follows Schema.org recommendations in order to enable better machine readability and indexing.  