---
title: Upload Your Metadata
stub: upload
section: metadata
section_order: 7
---

{:.py-4 .mt-4 #upload}
***

## 7. Uploading Your Metadata

1. **Get your metadata ready for upload:**
    - Once you've finished creating your metadata in Google Sheets (or another software program), click "File" and select "Download as Comma-separated values."
    - Locate the metadata CSV you've just downloaded on your computer. 
    - Without opening it, name this file using all lowercase letters, no spaces, and no hyphens.
    - Example filenames: `idahowater.csv`, `hjccc_dev.csv`

2. **Upload your metadata:**

<div id="accordion" class="mb-4">
<div class="card">
<div class="card-header" id="headingOne">
<h5 class="mb-0">
<button class="btn btn-link" data-toggle="collapse" data-target="#collapseOne" aria-expanded="true" aria-controls="collapseOne">
For GH Users
</button>
</h5>
</div>
<div id="collapseOne" class="collapse" aria-labelledby="headingOne" data-parent="#accordion">
<div class="card-body" markdown="1">
- Navigate to the _data director on the GitHub.com repository. 
- Click the "Upload Files" button at the top of the page.
- Open your File Explorer (PC) or Finder (Mac) and locate the CSV you just downloaded and renamed (it's probably in your "Downloads" folder). 
- Drag the file onto the web page. 
- Write a short commit message and then click the green "Commit changes" button at the bottom of the page.
</div>
</div>
</div>
<div class="card">
<div class="card-header" id="headingTwo">
<h5 class="mb-0">
<button class="btn btn-link collapsed" data-toggle="collapse" data-target="#collapseTwo" aria-expanded="false" aria-controls="collapseTwo">
For CDM and SA Users
</button>
</h5>
</div>
<div id="collapseTwo" class="collapse" aria-labelledby="headingTwo" data-parent="#accordion">
<div class="card-body" markdown="1">
- Open your CollectionBuilder repository in Visual Studio Code (see the [GitHub](github.html) instructions page if you need a refresher on how to do this).
- Open your File Explorer (PC) or Finder (Mac) and locate the CSV you just downloaded and renamed (it's probably in your "Downloads" folder). 
- Drag and drop this file into the repository you have open in Visual Studio Code, making sure to drop it directly into the `_data` directory. 
</div>
</div>
</div>

{% include bootstrap/alert.md color="warning mt-4" text="***Note: Do not confuse the `_data` directory with the `data` directory. Your metadata needs to go in the data directory with an underscore (`_`) in front of it.*** The /data/ directory is used to expose your collection as 'data' on the website." %}
