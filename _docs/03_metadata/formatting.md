---
title: Format Your Metadata
stub: format
section: metadata
section_order: 5
---

{:.py-4 .mt-4 #format}
***

<div class="row" markdown="1">
## 5. Formatting Your Metadata

<div class="col-md-7" markdown="1">
Make sure you're following the guidelines below, otherwise CollectionBuilder may not work.

- **Field Names Should Be Lowercase and Not Contain Special Characters**
    - Before you upload your metadata to CollectionBuilder, it is best practice to make all field names lowercase, since CollectionBuilder expects default fields to be lowercase. Preferably field names should not contain hyphens (`-`), spaces (` `), slashes (`/`, `\`), or special characters (`&`, etc.)--these won't necessarily break things, but might cause issues when fields are passed through javascript code!
- **Use a Semicolon When You Have Multiple Values**
    - Use a semicolon (`;`) to separate values in multi-valued fields.
- **No Special Characters in ID values**
    - When creating **objectids** and **filenames** do not use spaces (` `), slashes (`/`, `\`), and special characters (`&`). Since these values will be used in URLs, they should be web safe characters.

</div>

<div class="col-md-5" markdown ="1">
{% include bootstrap/alert.md color="primary" text="**Tip:** In Visual Studio Code, there's **an easy way to make your fields lowercase**: 
1. Highlight the first row of your CSV (the row containing field names) 
2. Click the 'Command Palette' option in the View menu 
3. Start typing 'Transform to lowercase'--the option will appear!" %}
</div>
</div>
