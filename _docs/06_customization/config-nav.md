---
title: Navigation
stub: config-nav
section: customize
section_order: 1
---

{:.py-4 .mt-4 #config-nav}
***

## Navigation Header Configuration (config-nav.csv)

This CSV controls what and in what order the links appear in your header's navigation bar. 

- **display_name**: This field determines what words will display in the nav bar. 
- **stub**: This field determines what link the display text will follow.  
- **dropdown_parent**: This field is used to add dropdown functionality to your nav bar. Use it to indicate items that should appear inside a dropdown menu. It should be left empty for any non-dropdown nav item. Follow these rules to configure your nav dropdown:
    - If the item has a `stub`, but no value in `dropdown_parent`, it becomes a normal nav item
    - If the item has no `stub`, it will become a dropdown menu
    - If the item has a value in `dropdown_parent`, it will only show up under its parent dropdown

### Example

{:.pl-4}
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


The above CSV will create 7 links in the nav bar for the referenced pages. These same nav items will also automatically appear in the footer. The last two lines of this CSV will appear within the "About" dropdown menu. "About" (because it has no value in `stub` or `dropdown_parent`) will appear in the nav bar as a dropdown button. When clicked, the dropdown menu will appear with "About the Collection" and "CollectionBuilder" listed, both linking to their respective pages.

You might have noticed that the Locations Page has been deleted, so it won't show up in your nav bar. If you want to add it back in, you'll just need to add a line after the `Subjects,/subjects.html,` line that reads: `Locations,/locations.html,`

Note: Dropdowns do NOT appear in the footer nav. The parent will appear, with a link to the top child. 