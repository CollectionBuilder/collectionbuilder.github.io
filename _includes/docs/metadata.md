[Our Metadata Page]({{'/metadata/' | relative_url}}) should help you investigate all our recommendations for the metadata. 

CollectionBuilder has some metadata standards and formats that you'll need to follow in order for the site to work correctly. Follow the steps below to get your metadata ready.

1. [Metadata Template](#template)
2. [Required Fields](#required)
3. [Fields for Visualizations](#vis)
4. [Recommended Fields](#recommend)
5. [Formatting Your Spreadsheet](#)
6. [Uploading Your Metadata](#)
7. [Troubleshooting](#)


{:.py-4 .mt-4 #template}
***

## 1. Metadata Template
To prevent formatting errors that can result from using software like Microsoft Excel, we recommend editing your metadata in Google Sheets. If your data will require a good amount of wrangling to get it into CollectionBuilder's format, we suggest you use [OpenRefine](http://openrefine.org/){:target="_blank"}, a platform that facilitates large scale data cleaning and transformation.  

The first step is to make sure your metadata fields are titled according to the [CollectionBuilder Metadata Template](https://docs.google.com/spreadsheets/d/14iWUEoAJ6T9WDqlPnIHRN7M8-YgmMV4_bjFPVuSZ0yk/edit?usp=sharing). Our template contains an example record to demonstrate the data format for each field. For a more detailed description of how each format is defined and mapped, see the [CollectionBuilder Data Dictionary](/assets/data_dictionary.pdf)

We recognize that each collection is different and may require metadata fields other than those in our template. We'll talk more about how you can add these in later in the Customization section. For now, we want to be sure you start with the fields required for CollectionBuilder to work.

{:.py-4 .mt-4 #required}
***

## 2. Required Fields 
Without values in these fields, CollectionBuilder will not work properly.

- **objectid**:
    - This should be a unique string with no spaces or special characters. Underscores are okay, hyphens aren't.
    - Example: `coll002`
- **cdmid** (for CONTENTdm skin):
    - This is the unique identification number assigned to the item by CONTENTdm. Optimally, this should coincide with the item's objectid (ex. **objectid**: `coll002`, **cdmid**: `2`), but this correspondence is not necessary for CollectionBuilder to work.
    - Example: `2`
- **title**: 
    - The title field is used to indicate the name of an item. This should be a short, descriptive set of words that identify the item. Each item may only have one title.
    - Example: `Haystack Rock`
- **format**: 
    - This field indicates the item's media type and is the most important field for setting up the various displays and interactive visualizations. Without it, some visualizations will not work and you won't be able to browse based on item format. The input for this field should be structured according to MIME type standards, consisting of a type and a subtype concatenated with a slash (`/`) between them. The most common options for this field are listed below, but you can also [read more about other MIME types](https://www.iana.org/assignments/media-types/media-types.xhtml){:target="_blank"}.
        - Image: `image/jpeg`
        - Document: `application/pdf`
        - Audio: `audio/mp3`
        - Video: `video/youtube`

{:.py-4 .mt-4 #vis}
***

## 3. Visualization Fields
CollectionBuilder uses these fields to generate contextual visualizations, including a map, timeline, and word clouds reflecting the frequency of subjects and locations in a collection.

- **latitude**:
    - A geographic coordinate specifying the north-south position of an item. See our page on the map visualization to learn how to find lat/longs for your items.
    - Example: `46.731643`
- **longitude**:
    - A geographic coordinate specifying the north-south position of an item. See our page on the map visualization to learn how to find lat/longs for your items.
    - Example: `-117.165625`
- **date**: 
    - This field indicates a point in time or period of time associated with the item. Date should always be in the format `yyyy-mm-dd`, which will enable our various timeline visualizations. See our Timeline page for more details. For less exact dates, `yyyy-mm` or `yyyy` may be used.
    - Example: `1997-07-16`
- **subject**:
    - The subject field contains topic(s) related to the item. This field allows for multiple subjects to be input for a single record. Each should be separated with a semi-colon (`;`). *Note: This field needs to be named 'subject' (not 'subjects')* for CollectionBuilder to work. Data in this field will create the word cloud that allows visualizations of the amount of subjects used within the collection. See our Subject page for more information.
    - Example: `Dogs; Cats; Zebras`
- **location**: 
    - This field designates a geographic location(s) to which the item is tied. Much like the subject field, this field will build a tag cloud of the most used locations in your collection. See the location page for more information. Be sure to separate multiple location entries for a single record with a semi-colon (`;`).
    - Example: `Pullman, Washington; Moscow, Idaho`

{:.py-4 .mt-4 #recommend}
***

## 4. Recommended Fields
The rest of the fields in the CollectionBuilder metadata template are not required for CollectionBuilder or its visualizations to work, but their use is highly encouraged to ensure a richly informative collection. These remaining fields are listed below, along with their respective definitions and examples.

- filename:
- creator:
- description:
- collection:
- identifier:
- type:
- language: 
- rights:
- rightsstatement:


Before you upload your metadata to CollectionBuilder, make sure **all field titles are lowercase**. CollectionBuilder will not work if the field titles are not lowercase. If you are using Visual Studio Code, highlight the first row of your CSV (the row containing field titles) and use the keyboard shortcut `ctrl shift p` for PC or `cmd shift p` for Mac to make field titles lowercase.

**In general, follow these rules when inputting metadata**
- Use a semi-colon (`;`) to separate values in multi-valued fields
- When creating objectids, filenames, and identifers, avoid including hyphens (`-`), spaces (` `), and special characters (`&`)

***WARNING: At this time, CONTENTdm's compound objects are not supported in CollectionBuilder***
- If you have compound objects, link to as an entire pdf.

**Common problems with metadata**



Abbreviated Data Dictionary as a table?