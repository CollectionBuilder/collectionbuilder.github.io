{:.py-4 .mt-4 #config-metadata}
***

## Metadata / Item Page Configuration (config-metadata.csv)

The most important CSV (if you're measuring by the number of pages it creates!) is the one that controls the metadata. [***config-metadata.csv***](#config-metadata) controls how an item's metadata is displayed on its web page. The file provides a number of options to help control the display of the item, as well as the machine-readability/SEO indexing characteristics of the code underneath the display. The fields are described below: 

- **field**: This variable corresponds to the field listed in the metadata for the collection. For instance, if you have a field called "original-collection", you would put "original-collection" here. 
- **display-name**: This variable is how you'd like the field to be described on the item page. So, using the example above, if you'd like the field "original-collection" to appear as "Original Archival Collection" on the item page, you'd enter "Original Archival Collection" in the second column. 
- **dc-map**: 
    - *Options*: [DC Terms](https://www.dublincore.org/specifications/dublin-core/dcmi-terms/), written like "DC.the_term_you_choose_from_the_site_linked
    - If you'd like to map this piece of metadata so that it will be machine readable in the code for the page, you can enter the Dublin Core metadata field you'd like it to be represented as here. So, continuing with our example, if you'd lke to map the "original-collection" field to be read as a Dublin Core Source element, you'd enter "DC.source" in the third column.  
- **browse-link**: 
    - *Options*: "true" or leave blank. 
    - You can either enter "true" in this column, or leave it blank. This option controls whether this element will be represented as a link back to the browse page. It is most useful for those fields, like "subject," that often have multiple entries. So, for instance, if you wanted to make the subjects in your "subject" field separate out into individual links, you'd enter "true" in the fourth column. 

### Example 

{:.pl-4}
    field,display-name,dc-map,browse-link
    title,Title,DC.title
    creator,Creator,DC.creator
    date,Date Created,DCTERMS.created
    description,Description,DC.description
    subject,Subjects,DC.subject,true
    location,Locations,,true
    collection,Source Collection,DC.source
    type,Type,DC.type
    format original,Original Format
    format,Format

- All fields in the above would be textual, save for the location and subject fields, which would create filter links (e.g. browse.html#dogs) back to the browse page for each location and subject delimited by semi-colon in that field. 

- The title, creator, data, description, subject, collection, type, and format fields would all be represented in the web page's "head" meta section related to the Dublin Core schema to enable better machine readability and indexing. 