---
title: Other Fields
stub: other
section: metadata
section_order: 5
---

{:.py-4 .mt-4 #other}
***

## 5. Other Fields
There are three fields that are specific to particular versions of CollectionBuilder or media formats and should only be included in the following situations:

- **youtubeid** *(Only required if your collection contains YouTube videos)*:
    - This is the unique string assigned to a video when it is uploaded to YouTube. An easy way to find this is to look at the url for your YouTube video. The ID will be the string attached to the end of this url: https://www.youtube.com/watch?v=
    - Example Input: `sHhk1eAgopU`

{%include bootstrap/alert.md color="warning ml-4 font-small" text="*The option below is only for the **CDM** skin. The feature is currently in development and not available as of March 2020.*"%}

- **collectionid** *(Only required if you are pulling in multiple CONTENTdm collections using the CollectionBuilder-CONTENTdm version)*:
    - This is the collection alias assigned by a collection creator in CONTENTdm.
    - Example Input: `archivalidaho`
