---
title: Browse
stub: config-browse
section: customize
section_order: 3
---

{:.py-4 .mt-4 #config-browse}
***

## Browse Page Configuration (config-browse.csv)

The Browse page displays each item in the collection as a "card," which is a design feature common to Bootstrap. At the top of the page, a search box allows users to limit the display by searching for certain terms. We also use subject links throughout the site that link back into the browse page and filter the collection based on the filter chosen. 

So, for instance, if on the Subjects page, you clicked a button for "Forests," you would actually be clicking a link whose url ended as "browse.html#forests." The Browse page would take anything after the hashtag ('#') and filter the collection's cards by it. 

The Browse page configuration CSV allows you to control which metadata appears on a card for each item. Title and date (if it's there) appear automatically. After that, you can add whatever metadata you'd like, as well as determine how that metadata will be displayed. 

- **field**: Selects the field from your metadata CSV.
- **display_name**: Determines the field name as it is displayed to users.
- **btn**: Determines whether the field displays as a button. 
    - *Options*: `true` or leave blank
    - `true` will turn all metadata in that field into buttons, and is recommend for fields that have multiple entries, like 'subject.' 
- **hidden**: Determines whether this field is hidden.
    - Useful when you don't want a metadata field to be visibly present on Browse page cards, but still want to filter for that field.

### Example 

{:.p-4 .bg-light .mb-4}
```
field,display_name,btn,hidden
date,Date,
description,,
subject,,true
location,,true
```



If you want to add a description to the browse cards, and label it "Description" on the user interface, you would include a value of `description` in the "field" column and then include `Description` as the value of that row's "displayName" column.

If you want to include items' descriptions on the browse cards but feel that including the label is unnecessary, you could simply include a value of `description` in the "field" column and then leave that row's "displayName" column blank. The above example embodies this approach.