[Our Metadata Page]({{'/metadata/' | relative_url}}) should help you investigate all our recomendations for the metadata. 

CollectionBuilder has some metadata standards and formats that you'll need to follow in order for the site to work correctly. Follow the steps below to get your metadata ready.

To prevent formatting errors that can result from using software like Microsoft Excel, we recommend editing your metadata in Google Sheets. If your data will require a good amount of wrangling to get it into CollectionBuilder's format, we suggest you use [OpenRefine](http://openrefine.org/){:target="_blank"}, a platform that facilitates large scale data cleaning and transformation.  

The first step is to make sure your metadata fields are titled according to the [CollectionBuilder Metadata Template](https://docs.google.com/spreadsheets/d/14iWUEoAJ6T9WDqlPnIHRN7M8-YgmMV4_bjFPVuSZ0yk/edit?usp=sharing). Our template contains an example record to demonstrate the data format for each field. For a more detailed description of how each format is defined and mapped, see the [CollectionBuilder Data Dictionary](/assets/data_dictionary.pdf)

We recognize that each collection is different and may require metadata fields other than those in our template. We'll talk more about how you can add these in later in the Customization section. For now, we want to be sure you start with the fields required for CollectionBuilder to work.

**Required Fields**: 

- objectid:
    - This should be a unique string with no spaces or special characters. Underscores are okay, hyphens aren't.
    - Example: `coll002`
- cdmid (for CONTENTdm skin)
    - This is the unique identification number assigned to the item by CONTENTdm. Optimally, this should cooincide with the item's objectid (ex. objectid: `coll002`, cdmid: `2`), but this correspondence is not necessary for CollectionBuilder to work.
    - Example: `2`
- title
- format: 
    - This field indicates the item's media type and is the most important field for setting up the various displays and interactive visualizations. Without it, some visualizations will not work and you won't be able to browse based on item format. The input for this field should be structured according to MIME type standards, consisting of a type and a subtype concatenated with a slash (`/`) between them. The most common options for this field are listed below according, but you can also [read more about MIME types](https://www.iana.org/assignments/media-types/media-types.xhtml){:target="_blank"}.
        - Image: `image/jpeg`
        - Document: `application/pdf`
        - Audio: `audio/mp3`
        - Video: `video/youtube`

There are also **optional but important elements** to be aware of: 

- latitude and longitude -- these are two separate fields that will enable the map view. See our page on the map visualization to learn how to find lat/longs for your items.
- date - Date should always be in the format **yyyy-mm-dd**, which will enable our various timeline visualiations. See our Timeline page for more details
- subject - the subject field will create the word cloud that allows visualizations of the amount of subjects used within the collection. *The field needs to be named 'subject' (not 'subjects')* for the visualization to work. See our Subject page for more information. 
- location - much like the subject field, this field will build a tag cloud of the most used locations in your collection. See the location page for more information. 


Warning for CDM data:
- Compound objects not currently supported (as warning box?)

Abbreviated Data Dictionary as a table?

Input requirements:
- Note about ; for multi-valued field
- avoid hyphens, spaces, special characters (not a standard requirement for cdm or other systems)
- ctrl/cmd shift p for making fields lowercase


"Common problems with metadata" section