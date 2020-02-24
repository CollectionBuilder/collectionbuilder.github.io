
{:.py-4 .mt-4 #upload}
***

## 7. Uploading Your Metadata

1. **Get your metadata ready for upload:**
    - Once you've finished creating your metadata in Google Sheets, click "File" and select "Download as Comma-separated values."
    - Locate the metadata CSV you've just downloaded on your computer. 
    - Without opening it, name this file using all lowercase letters, no spaces, and no hyphens.
    - Example filename: `idahowater.csv`

2. **Upload your metadata:**
    - Open your CollectionBuilder repository in Visual Studio Code (see the [GitHub](github.html) instructions page if you need a refresher on how to do this).
    - Open your File Explorer (PC) or Finder (Mac) and locate the CSV you just downloaded and renamed (it's probably in your "Downloads" folder). 
    - Drag and drop this file into the repository you have open in Visual Studio Code, making sure to drop it directly into the `_data` directory. 

{% include bootstrap/alert.md color="warning" text="***Note: Do not confuse the `_data` directory with the `data` directory. Your metadata needs to go in the data directory with an underscore (`_`) in front of it.*** The /data/ directory is used to expose your collection as 'data' on the website." %}

3. **Nice work!**
    - You can now move on to the [Config]({{'/workshop/config/' | relative_url}}) section of this workshop.
