---
title: Map
stub: config-map
section: customize
section_order: 4
---

{:.py-4 .mt-4 #config-map}
***

## Map Page Configuration (config-map.csv)

The config-map.csv determines what information displays on the pop-ups on the map. More on map search options can be found on the [theme page](theme.html#map-page)

- **field**: Determines the metadata field that is included on the pop-up. 
- **display_name**: Determines the label that is displayed for that field. 
- **search**: Determines whether the field is searchable. 
    - *Options*: `true` or leave blank

### Example 

{:.p-4 .bg-light .mb-4}
```
field,display_name,search
date,Date,true
creator,Creator,true
location,Location,true
```