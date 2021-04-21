---
title: Colors
stub: config-colors
section: customize
section_order: 6
---

{:.py-4 .mt-4 #config-colors}
***

## Theme Color Configuration (config-theme-colors.csv)

For simplicity, CollectionBuilder uses pre-compiled Bootstrap CSS.
However, to make basic theming possible, we have added some code in `_sass/_theme-colors.scss` based on Bootstrap Sass to generate custom color CCS for btn-, btn-outline-, text-, and bg- classes. 
The custom classes can override existing Bootstrap theme colors or create new color classes. 

By default, these options are not used.

To add custom colors, edit the two columns in the `_data/config-theme-colors.csv`:

- **color_class**: The name you'll use to designate the color (i.e. the part after the `-` in `btn-primary`).
    - example --> `primary`
- **color**: Add the color in hex code.
    - example --> `#4232a8`

Any "color_class" with a "color" value will generate a btn-, btn-outline-, text-, and bg- class for the color, e.g. `btn-primary`, `btn-outline-primary`, `text-primary`, and `bg-primary`. 
Any "color_class" with a blank "color" will be ignored.
For convenience, the standard Bootstrap theme colors are provided to fill in if desired, which will override the existing Bootstrap colors.
Adding a non-Bootstrap "color_class" will generate new custom btn colors.
E.g. "color_class" `special` will generate CSS for `.btn-special` and `.btn-outline-special`.

CollectionBuilder uses `btn-primary`, `btn-outline-primary`, `btn-success`, `btn-info`, `btn-outline-info`, `btn-outline-secondary`, `btn-light`, and `btn-outline-light` in page layouts, so overriding those styles will have immediate effects on the colors.
The nav elements use `bg-dark` and `text-dark` by default.


