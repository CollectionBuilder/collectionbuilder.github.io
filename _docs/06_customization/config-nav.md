---
title: Navigation Header Configuration (config-nav.csv)
stub: config-nav
section: customize
section_order: 1
---

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