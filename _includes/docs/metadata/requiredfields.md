
{:.py-4 .mt-4 #required}
***

## 2. Required Fields 
Without values in these fields, CollectionBuilder will not work properly.

- **objectid**:
    - This is the field that CollectionBuilder uses to identify each object. This should be a unique string with no spaces or special characters. Underscores are okay, hyphens aren't.
    - Example Input: `coll002`
- **title**: 
    - The title field is used to indicate the name of an item. This should be a short, descriptive set of words that identify the item. Each item may only have one title.
    - Example Input: `Haystack Rock`
- **format**: 
    - This field indicates the item's media type and is the most important field for setting up the various displays and interactive visualizations. Without it, some visualizations will not work and you won't be able to browse based on item format. The input for this field should be structured according to MIME type standards, consisting of a type and a subtype concatenated with a slash (`/`) between them.
        - Image: `image/jpeg`
        - Document: `application/pdf`
        - Audio: `audio/mp3`
        - Video: `video/mp4`

{:.cdm .typefilter}    
- **cdmid** (for CONTENTdm skin):
    - This is the unique identification number assigned to the item by CONTENTdm. Optimally, this should coincide with the item's objectid (ex. objectid: `coll002`, cdmid: `2`), but this correspondence is not necessary for CollectionBuilder to work.
    - Example Input: `2`