CollectionBuilder has some metadata standards and formats that you'll need to follow in order for the site to work correctly. Follow the steps below to get your metadata ready.

***At this time, CONTENTdm's compound objects are not supported in CollectionBuilder.*** *If you have a compound object, link to it as a complete pdf.* 


1. [Metadata Template](#template)
2. [Required Fields](#required)
3. [Fields for Visualizations](#vis)
4. [Recommended Fields](#recommend)
5. [Other Fields](#other)
6. [Formatting Your Spreadsheet](#format)
7. [Uploading Your Metadata](#upload)

{:.py-4 .mt-4 #template}
***


{% include bootstrap/alert.md color="info mb-4" text="**Before You Start:** To prevent formatting errors that can result from using software like Microsoft Excel, we recommend editing your metadata in Google Sheets. If your data will require a good amount of wrangling to get it into CollectionBuilder's format, we suggest you use [OpenRefine](http://openrefine.org/), a platform that facilitates large scale data cleaning and transformation." %}  

{:.py-4 .mt-4 }
## 1. Metadata Template


{% include bootstrap/button.md color="info col-md-5 float-right my-4 ml-4" text="CollectionBuilder Metadata Template" link="https://docs.google.com/spreadsheets/d/14iWUEoAJ6T9WDqlPnIHRN7M8-YgmMV4_bjFPVuSZ0yk/edit?usp=sharing" %}

The first step is to make sure your metadata fields are titled according to the [CollectionBuilder Metadata Template](https://docs.google.com/spreadsheets/d/14iWUEoAJ6T9WDqlPnIHRN7M8-YgmMV4_bjFPVuSZ0yk/edit?usp=sharing).  Our template contains an example record to demonstrate the data format for each field.

{% include bootstrap/button.md color="secondary col-md-5 float-right my-2 ml-4" text="CollectionBuilder Data Dictionary" link="/images/data_dictionary.pdf" %}

For a more detailed description of how each format is defined and mapped, see the [CollectionBuilder Data Dictionary](/images/data_dictionary.pdf)

We recognize that each collection is different and may require metadata fields other than those in our template. We'll talk more about how you can add these in later in the Customization section. For now, we want to be sure you start with the fields required for CollectionBuilder to work.

{:.py-4 .mt-4 #required}
***

## 2. Required Fields 
Without values in these fields, CollectionBuilder will not work properly.

- **objectid**:
    - This is the field that CollectionBuilder uses to identify each object. This should be a unique string with no spaces or special characters. Underscores are okay, hyphens aren't.
    - Example Input: `coll002`
- **cdmid** (for CONTENTdm skin):
    - This is the unique identification number assigned to the item by CONTENTdm. Optimally, this should coincide with the item's objectid (ex. objectid: `coll002`, cdmid: `2`), but this correspondence is not necessary for CollectionBuilder to work.
    - Example Input: `2`
- **title**: 
    - The title field is used to indicate the name of an item. This should be a short, descriptive set of words that identify the item. Each item may only have one title.
    - Example Input: `Haystack Rock`
- **format**: 
    - This field indicates the item's media type and is the most important field for setting up the various displays and interactive visualizations. Without it, some visualizations will not work and you won't be able to browse based on item format. The input for this field should be structured according to MIME type standards, consisting of a type and a subtype concatenated with a slash (`/`) between them.
        - Image: `image/jpeg`
        - Document: `application/pdf`
        - Audio: `audio/mp3`
        - Video: `video/mp4`

{:.py-4 .mt-4 #vis}
***

## 3. Fields Required for Visualizations
CollectionBuilder uses these fields to generate contextual visualizations, including a map, timeline, and word clouds reflecting the frequency of subjects and locations in a collection.

{%include bootstrap/card.md class="float-right col-md-5 ml-2 p-0" text="<table class='table table-striped'><tr><th>Page</th><th>Required Fields</th></tr><tr><td>Map</td><td>`latitude` & `longitude`</td></tr><tr><td>Timeline</td><td>`date` (yyyy at min.)</td></tr><tr><td>Subjects</td><td>`subject`</td></tr><tr><td>Location</td><td>`location`</td></tr></table>" %}


- **latitude**:
    - A geographic coordinate specifying the north-south position of an item. See the [Map](theme.html#map-page) section for more information.
    - Example Input: `46.731643`
- **longitude**:
    - A geographic coordinate specifying the east-west position of an item. See the [Map](theme.html#map-page) section for more information.
    - Example Input: `-117.165625`
- **date**: 
    - This field indicates a point in time or period of time associated with the item. 
    - Dates should always be represented in the format `yyyy-mm-dd`, which will enable our various timeline visualizations. See the [Timeline](theme.html#timeline-page) section for more details. 
    - For less exact dates, `yyyy-mm` or `yyyy` may be used.
    - Example Input: `1997-07-16`, `1997-07`, `1997`
- **subject**:
    - The subject field contains topic(s) related to the item. 
    - This field allows for multiple subjects to be input for a single record. Each should be separated with a semi-colon (`;`). 
    - See the [Subjects](theme.html#subjects-page) section for more information.
    - Example Input: `Dogs; Cats; Zebras`
{%include bootstrap/alert.md color="warning ml-4 font-small" text="*Note: This field needs to be named ***'subject' (not 'subjects'***) for many features in CollectionBuilder to work.* Data in this field will create the word cloud that allows users to visualize the amount of subjects used within the collection."%}
- **location**: 
    - This field designates a geographic location(s) to which the item is tied. Much like the subject field, this field will build a tag cloud of the most used locations in your collection. See the [Locations](theme.html#locations-page) section for more information. Be sure to separate multiple location entries for a single record with a semi-colon (`;`).
    - Example Input: `Pullman, Washington; Moscow, Idaho`

{:.py-4 .mt-4 #recommend}
***

## 4. Optional Fields
The rest of the fields in the CollectionBuilder metadata template are not required for CollectionBuilder or its visualizations to work, but their use is encouraged to ensure a richly informative collection. These remaining fields are listed below, along with their respective definitions and examples.

{% include bootstrap/alert.md color="info" text="*CollectionBuilder can accommodate any field you list in your metadata.  You can list any field on item pages or on our browse cards on the home page. See the [Metadata](customize.html#config-metadata) and [Browse](customize.html#config-metadata) customization sections for more information.* "%}

- **creator**:
    - The creator property designates an entity primarily responsible for making the resource. Mutliple creators may be input, as long as each is separated by a semi-colon (`;`).
    - Example Input: `Smith, John` or `Smith, John; Doe, Jane`
- **description**:
    - The description should be a brief account of the object. Each object should only have one description.
    - Example Input: `Postcard of the Memorial Gymnasium on the University of Idaho campus in Moscow, Idaho.`
- **source**:
    - The source field designates a related source collection or resource from which the object is derived. This field is especially relevant for digitized archival collections. In such a situation, the name of the physical archival collection would be the input for this field. The input should be expressed as the collection name followed by a comma, then followed by the holding library.
    - Example Input: `PG 5, University of Idaho Library Special Collections and Archives`
- **identifier**:
    - The identifier field is used to preserve the unique identifier assigned to the object by the object's (usually physical) source collection.
    - Example Input: `ARG-02-16-1993`
- **type**:
    - An object's type distinguishes between types of image, sound, text, etc. using a one- or two-value input. At minimum, the input should contain a value chosen from the [DCMI Type Vocabulary](https://www.dublincore.org/specifications/dublin-core/dcmi-type-vocabulary/2003-02-12/){:target="_blank"}. If using a second value, the second value does not need to relate to a controlled vocabulary, but should give further specification of the object type. The two values in a pair should be separated by a semi-colon (`;`). See examples below.
    - Example Input: `Image;StillImage`, `Image;MovingImage`, `Text`, `Sound`
- **language**: 
    - This field indicates the language associated with the object. Recommended best practice is to use a controlled vocabulary such as the [ISO 639-2 Codes for the Representation of Names and Languages](http://www.loc.gov/standards/iso639-2/php/code_list.php){:target="_blank"} to designate language tags.
    - Example Input: `en`, `fr`, `de`
- **rights**:
    - The rights field should include a free-text rights statement describing information about rights held in and over the object.
    - Example Input: `Educational use includes non-commercial use of text and images in materials for teaching and research purposes. Digital reproduction rights granted by the University of Idaho Library. For other uses beyond free use, please contact University of Idaho Library Special Collections and Archives Department.`
- **rightsstatement**:
    - This field is a standardized rights statement, designated in the form of a URI. It should be presented as a creativecommons.org URI or a rightsstatements.org URI.
    - Example Input: `http://rightsstatements.org/vocab/NoC-US/1.0/`


{:.py-4 .mt-4 #other}
***

## 5. Other Fields
There are three fields that are specific to particular versions of CollectionBuilder or media formats and should only be included in the following situations:

- **youtubeid** *(Only required if your collection contains YouTube videos)*:
    - This is the unique string assigned to a video when it is uploaded to YouTube. An easy way to find this is to look at the url for your YouTube video. The ID will be the string attached to the end of this url: https://www.youtube.com/watch?v=
    - Example Input: `sHhk1eAgopU`

{%include bootstrap/alert.md color="warning ml-4 font-small" text="*The two options below are currently in development and not available as of October 2019.*"%}

- **collectionid** *(Only required if you are pulling in multiple CONTENTdm collections using the CollectionBuilder-CONTENTdm version)*:
    - This is the collection alias assigned by a collection creator in CONTENTdm.
    - Example Input: `archivalidaho`

- **fileid** *(Only required if you are using the CollectionBuilder-Standalone version, which is under development)*:
    - This is the digital object's filename, including the name itself as well as the object's file extension. Each filename property should have a single value and end with a file extension.
    - *Common Extension Options*: `.jpg`, `.pdf`, `.mp3`
    - Example Input: `pg1_440.jpg`

{:.py-4 .mt-4 #format}
***

## 6. Formatting Your Metadata
{% include bootstrap/alert.md color="primary col-md-4 float-right ml-4 mb-4 mt-2" text="**Tip:** In Visual Studio Code, there's **an easy way to make your fields lowercase**: 
1. Highlight the first row of your CSV (the row containing field titles) 
2. Click the 'Command Pallette' option in the View menu 
3. Start typing 'Transform to lowercase'--the option will appear!" %}

Make sure you're following the guidelines below, otherwise CollectionBuilder will not work.

- **Field Titles Need To Be Lowercase**
    - Before you upload your metadata to CollectionBuilder, make sure **all field titles are lowercase**.
    - CollectionBuilder will not work if the field titles are not lowercase. 

- **Use a Semi-colon When You Have Multiple Values**
    - Use a semi-colon (`;`) to separate values in multi-valued fields

- **Avoid Special Characters**
    - When creating **objectids**, **filenames**, and **identifers**, avoid using hyphens (`-`), spaces (` `), and special characters (`&`)


{:.py-4 .mt-4 #upload}
***

## 7. Uploading Your Metadata

1. **Get your metadata ready for upload:**
    - Once you've finished creating your metadata in Google Sheets, click "File" and select "Download as Comma-separated values."
    - Locate the metadata CSV you've just downloaded on your computer. 
    - Without opening it, name this file using all lowercase letters, no spaces, and no hyphens.
    - Example filename: `idahowater.csv`

2. **Upload your metadata:**
    - Open your CollectionBuilder repository in Visual Studio Code (see the [GitHub](github.html) instructions page if you need a refresher on how to do this).
    - Open your File Explorer (PC) or Finder (Mac) and locate the CSV you just downloaded and renamed (it's probably in your "Downloads" folder). 
    - Drag and drop this file into the repository you have open in Visual Studio Code, making sure to drop it directly into the `_data` directory. 

{% include bootstrap/alert.md color="warning" text="***Note: Do not confuse the `_data` directory with the `data` directory. Your metadata needs to go in the data directory with an underscore (`_`) in front of it.*** The /data/ directory is used to expose your collection as 'data' on the website." %}

3. **Nice work!**
    - You can now move on to the [Config]({{'/workshop/config/' | relative_url}}) section of this workshop.
