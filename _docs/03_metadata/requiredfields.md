---
title: Required Fields
stub: required
section: metadata
section_order: 2
---

{:.py-4 .mt-4 #required}
***

## 2. Required Fields 

Without values in the fields below, CollectionBuilder will not work properly.

- **objectid**:
    - This is the field that CollectionBuilder uses to identify each object. This should be a unique string with no spaces or special characters as it will used to form the item's URL. Underscores (`_`) are okay; **slashes (`/`) should NOT be used in this field**.
    - Example value: `coll002`
- **title**: 
    - The title field is used to indicate the name of an item. This should be a short, descriptive set of words that identify the item. Each item may only have one title.
    - Example value: `Haystack Rock`
- **format**: 
    - This field indicates the item's media type. Since CollectionBuilder uses logic based on `format` to display objects, this is the most important field to ensure the interactive visualizations function correctly. If there are errors or anomalies, some pages will not work. The input for this field should be structured according to [MIME type](https://www.iana.org/assignments/media-types/media-types.xhtml){:target="_blank" rel="noopener"} standards, consisting of a type and a subtype concatenated with a slash (`/`) between them.
        - Image: `image/jpeg`
        - Document: `application/pdf`
        - Audio: `audio/mp3`
        - Video: `video/mp4`

#### Required Fields for YouTube Objects

- **youtubeid** *(Only required if your collection contains YouTube videos)*:
    - This is the unique string assigned to a video when it is uploaded to YouTube. An easy way to find this is to look at the url for your YouTube video. The ID will be the string attached to the end of this url: https://www.youtube.com/watch?v=
    - Example value: `sHhk1eAgopU`

#### Required Fields for GH and SA

- **filename**: 
    - This is the digital object's filename, including the name itself as well as the object's file extension. Each filename property should have a single value and end with a file extension. 
    - The filename should be a **lowercase unique string with no spaces or special characters**. Underscores (`_`) are okay; **slashes (`/`) and hyphens (`-`) should NOT be used in this field**. 
    - Records for YouTube objects will not usually have a value in this field. 
    - *Common Extension Options*: `.jpg`, `.pdf`, `.mp3`
    - Example value: `letter001.pdf`

#### Required Fields for CONTENTdm

{:.cdm .typefilter}    
- **cdmid** (for CONTENTdm skin):
    - This is the unique identification number assigned to the item by CONTENTdm (the field titled "CONTENTdm number" in your exported metadata). For convenience, we generally make this correspond with the number in the item's objectid (ex. objectid: `coll002`, cdmid: `2`), but this correspondence is not necessary for CollectionBuilder to work.
    - Example value: `142`

***At this time, CONTENTdm's compound objects are not supported in CollectionBuilder.*** *If you have a compound object, link to it as a complete pdf.*
