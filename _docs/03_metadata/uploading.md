---
title: Upload Your Metadata
stub: upload
section: metadata
section_order: 6
---

{:.py-4 .mt-4 #upload}
***

## 6. Uploading Your Metadata

{% include bootstrap/alert.md color="warning mt-4" text="*Note:* CSV metadata should be in UTF-8 encoding. CSV's downloaded from Google Sheets or exported from OpenRefine will have the correct encoding. However, Excel does not handle UTF-8 correctly, and may cause issues." %}

1. **Get your metadata ready for upload:**
    - Once you've finished creating your metadata in Google Sheets (or other software), click "File" and select "Download as Comma-separated values."
    - Locate the metadata CSV you've just downloaded on your computer. 
    - Without opening it, name this file using all lowercase letters, no spaces, and no hyphens.
    - Example filenames: `idahowater.csv`, `hjccc_dev.csv`
2. **Upload your metadata:**

<div id="accordion" class="mb-4">
<div class="card">
<div class="card-header" id="headingOne">
<h5 class="mb-0">
<button class="btn btn-link text-dark" data-toggle="collapse" data-target="#collapseOne" aria-expanded="true" aria-controls="collapseOne">
For GH Users
</button>
</h5>
</div>
<div id="collapseOne" class="collapse" aria-labelledby="headingOne" data-parent="#accordion">
<div class="card-body" markdown="1">
1. Navigate to the _data directory on the GitHub.com repository. 
2. Click the "Upload Files" button at the top of the page.
3. Open your File Explorer (PC) or Finder (Mac) and locate the CSV you just downloaded and renamed (it's probably in your "Downloads" folder). 
4. Drag the file onto the web page. 
5. Write a short commit message and then click the green "Commit changes" button at the bottom of the page.
</div>
</div>
</div>
<div class="card">
<div class="card-header" id="headingTwo">
<h5 class="mb-0">
<button class="btn btn-link collapsed text-dark" data-toggle="collapse" data-target="#collapseTwo" aria-expanded="false" aria-controls="collapseTwo">
For CDM and SA Users
</button>
</h5>
</div>
<div id="collapseTwo" class="collapse" aria-labelledby="headingTwo" data-parent="#accordion">
<div class="card-body" markdown="1">
1. Locate the CSV you just downloaded and renamed (it's probably in your "Downloads" folder) in your File Explorer / Finder
2. Copy (or drag and drop) the metadata file into your CollectionBuilder project repository's "_data" directory (your repository is probably in your Documents > GitHub folder). 
3. Commit the new metadata using Git or GitHub Desktop.
</div>
</div>
</div>

{% include bootstrap/alert.md color="warning mt-4" text="***Note: Do not confuse the `_data` directory with the `data` directory. Your metadata needs to go in the data directory with an underscore (`_`) in front of it.*** The /data/ directory is used to expose your collection as 'data' on the website." %}
