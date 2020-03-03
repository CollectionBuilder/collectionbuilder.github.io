---
title: Metadata
stub: config-metadata
section: customize
section_order: 2
---

{:.py-4 .mt-4 #config-metadata}
***

## Metadata / Item Page Configuration (config-metadata.csv)

The most important CSV (if you're measuring by the number of pages it creates!) is the one that controls the metadata. The [***config-metadata.csv***](#config-metadata) controls how an item's metadata is displayed on its web page. The file provides a number of options to help control the display of the item, as well as the machine-readability/SEO indexing characteristics of the code underneath the display. The fields are described below: 

- **field**: This variable corresponds to the field listed in the metadata for the collection. For instance, if you have a metadata field called "original-collection", you would put "original-collection" here. 
- **display_name**: This variable is how you'd like the field to be described on the item page. So, using the example above, if you'd like the field "original-collection" to appear as "Original Archival Collection" on the item page, you'd enter "Original Archival Collection" in the second column.
- **browse_link**: 
    - *Options*: `true` or leave blank. 
    - You can either enter `true` in this column, or leave it blank. This option controls whether this element will be represented as a link from the item page back to the browse page. It is most useful for those fields, like "subject," that often have multiple entries. So, for instance, if you wanted to make the subjects in your "subject" field separate out into individual links, you'd enter `true` in the fourth column of the `config-metadata.csv`  
{% include bootstrap/alert.md text="**GH Users, please note**: 'browse_link' is included in **GH's config-metadata.csv**, but **does not work yet**. This capability will be implemented for GH in the future." color="info" %}
- **dc_map**: 
    - *Options*: [DC Terms](https://www.dublincore.org/specifications/dublin-core/dcmi-terms/), written like `DC.the_term_you_choose_from_the_site_linked`
    - If you'd like to map this piece of metadata so that it will be machine readable in the code for the page, you can enter the Dublin Core metadata field you'd like it to be represented as here. So, continuing with our original example, if you'd lke to map the "original-collection" field to be read as a Dublin Core Source element, you'd enter "DC.source" in the third column.
- **schema_map**:
    - Schema is a standard designed to provide structured semantic markup for search engines to better understand content of web pages. Item pages have in depth Schema markup in JSON-LD format driven by the object metadata. 
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

{:.pl-4}
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

- In the case of this example:
    - Only the location and subject fields have a value (`true`) for "browse-link", which creates filter links (e.g. browse.html#dogs) back to the browse page for each location and subject delimited by semi-colon in that field. 
    - The title, creator, date, description, subject, and type fields would all be represented in an item page's "head" meta section related to the Dublin Core schema to enable better machine readability and indexing.
    - The title, creator, date, description, subject, location, format, and rightstatement fields would all be represented in an item page's "head" meta section related to Schema.org to enable better machine readability and indexing.  