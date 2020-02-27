---
title: Browse Page Configuration (config-browse.csv)
stub: config-browse
section: customize
section_order: 3
---

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