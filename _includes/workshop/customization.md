 Refer to the [.theme.yml section](theme.html) for more information about customizing the various pages in your collection. 

The files discussed in this section will help you customize the website to fit the metadata that's driving it. Each of these files is a CSV (comma separated values) file that is stored in the /_data/ directory of your repository. You can edit this using your text editor (recommended) or you can edit them using Google Sheets or another spreadsheet program (that supports UTF-8 encoding).

- [Navigation Header Configuration](#config-nav) (config-nav.csv)
    - configure the navigation links in the header
- [Metadata / Item Page Configuration](#config-metadata) (config-metadata.csv)
    - configure how metadata appears on item pages
- [Browse Page Configuration](#config-browse) (config-browse.csv)
    - configure the information on the browse cards for items
- [Map Page Configuration](#config-map) (config-map.csv)
    - configure what appears in the map pop-ups
- [Table Configuration](#config-table) (config-table.csv)
    - configure what metadata appears in the table visualization

{:.py-4 .mt-4 #config-nav}
***

## Navigation Header Configuration (config-nav.csv)

This CSV controls what and in what order the links on your header show up. 

- **display-text**: This field determine what words will display in the header. 
- **stub**: This field determins what link the display text will follow. 

### Example

{:.pl-4}
    display-text,stub
    Home,/
    Browse,/browse.html
    Subjects,/subjects.html
    Map,/map.html
    Timeline,/timeline.html
    Data,/data/

The above CSV would create 6 links in the header for the referenced pages. Note the About Page has been deleted. If you wanted to add it back in, you'd just add a line after the "Data,/data/" line that read: About,about.html

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

- All fields in the above would be textual, save for the location and subject fields, which would create filter links (e.g. browse.html#dogs) back to the browse page for each location and subject delimited by semicolon in that field. 

- The title, creator, data, description, subject, collection, type, and format fields would all be represented in the web page's "head" meta section related to the Dublin Core schema to enable better machine readability and indexing.   
 
{:.py-4 .mt-4 #config-browse}
***

## Browse Page Configuration (config-browse.csv)

The Browse page displays all the items in the collection as a "card," which is a design feature common to Bootstrap. At the top of the page, a search box allows users to limit the display by searching for certain terms. We also use subject links throughout the site that link back into the browse page and filter the collection based on the filter choosen. 

So, for instance, if on the Subjects page, you clicked a button for "Forests," you would actually be clicking a link whose url ended as "browse.html#forests." The Browse page would take anything after the hashtag ('#') and filter the collection's cards by it. 

The Browse page configuration CSV allows you to control which metadata appears on a card for each item. Title and date (if it's there) appear automatically. After that, you can add whatever metadata you'd like, as well as determine how that metadata will be displayed. 

- **field** - determines the field that is displayed
- **display-name** - 
- **btn** - Determines whether that metadata displays as a button or if it should be prefaced by a label. 
    - *Options*: either "btn" or any other text you'd like to use as a label for the field. 
    - "btn" will all metadata in that field into buttons, and is recommend for fields that have mutiple entries, like 'subject.' 
- **hidden** - 

To turn the metadata in a field, such as the 'subject' field, into buttons that encourage the user to click them and filter the collection by that term, you simply need to define the field in the first column and then write "btn" in the second column. So, for a subject field, that would look like: "subject,btn" . 

If you wanted to add, for instance, a description, and call that a description, you would write "description,Description" and if you wanted to include the description but you thought labelling it was unnecessary, you could write "description," and thereby leaving the display name blank. 



{:.py-4 .mt-4 #config-map}
***

## Map Page Configuration (config-map.csv)

The config-map.csv determines what information displays on the pop-ups on the map. More on the search option can be found on the [theme page](theme.html#map-page)

- **field** - Determines the field that is displayed on the pop-up. 
- **display** - Determines the label given to the field. 
- **search** - Determines whether the field is searchable. 
    - *Options*: 'true' or leave blank

{:.py-4 .mt-4 #config-table}
***

## Table Configuration (config-table.csv)

The table appears on the "Data" page. It uses [DataTables](https://datatables.net/) to generate a table that can be searched, sorted, and downloaded as a whole or in a filtered version.

We recommend not using more than 5 or 6 fields here, as the table can become overcrowded. 

- **field** - Determines the field that is displayed on the pop-up. 
- **display** - Determines the label given to the field. 