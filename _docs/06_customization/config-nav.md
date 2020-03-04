---
title: Navigation
stub: config-nav
section: customize
section_order: 1
---

{:.py-4 .mt-4 #config-nav}
***

## Navigation Header Configuration (config-nav.csv)

This CSV controls what and in what order the links appear in your collection's navigation bar. 

- **display_name**: This field determines what words will display in the nav bar. 
- **stub**: This field determines what link the display text will follow.  
- **dropdown_parent**: This field is used to add dropdown functionality to your nav bar. Use it to indicate items that should appear inside a dropdown menu. It should be left empty for any non-dropdown nav item. Follow these rules to configure your nav dropdown:
    - If the item has a `stub`, but no value in `dropdown_parent`, it becomes a normal nav item
    - If the item has no `stub`, it will become a dropdown menu
    - If the item has a value in `dropdown_parent`, it will only show up under its parent dropdown

### Example

{:.p-4 .bg-light}
```
display_text,stub,dropdown_parent
Home,/,
Browse,/browse.html,
Subjects,/subjects.html,
Map,/map.html,
Timeline,/timeline.html,
Data,/data/,
About,,
About the Collection,/about.html,About
CollectionBuilder,/tech.html,About
```


**Some Explaining** 

The above CSV will create 7 links in the nav bar for the referenced pages. These same nav items will also automatically appear in the footer. 

You might have noticed that the Locations Page has been deleted, so it won't show up in your nav bar. If you want to add it back in, you'll just need to add a line after the `Subjects,/subjects.html,` line that reads: `Locations,/locations.html,`

**How the Dropdown Works**

The last two lines of this CSV will appear within the "About" dropdown menu. To enable this, "About" must have no value in `stub` or `dropdown_parent` cells--this will direct the code to make "About" a dropdown button and store any link that lists "About" as it's `dropdown_parent` in its dropdown menu. So in the above, when About is clicked the dropdown menu will appear with "About the Collection" and "CollectionBuilder" listed, both linking to their respective pages.

Note: Dropdowns do NOT appear in the footer nav. The parent will appear, with a link to the top child. 