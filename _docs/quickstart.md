---
title: Quick Start
stub: intro
section: quickstart
section_order: 0
---

## CollectionBuilder-GH

For those who can't wait, below are six quick steps to get you started.

1. Import <a href="https://github.com/CollectionBuilder/collectionbuilder-gh" target="_blank" rel="noopener">the CollectionBuilder GitHub repository </a> into your own GitHub repository.
2. Download the <a href="https://docs.google.com/spreadsheets/d/1Uv9ytll0hysMOH1j-VL1lZx6PWvc1zf3L35sK_4IuzI/edit#gid=0" target="_blank" rel="noopener">Metadata Template</a>.
3. Follow the formatting of the example record in the template to fill in metadata on your own objects.
4. Upload your files into the "Objects" folder in your repository<a target="_blank" rel="noopener" href="https://help.github.com/en/articles/configuring-a-publishing-source-for-github-pages">
5. Turn on GitHub Pages</a> for the Repository Check out your site via the link provied on your repository's setting's page!

## Skin - CONTENTdm

For those who can't wait, below are six quick steps to get you started.</p>
1. Make sure you have Git, Ruby, and Jekyll Installed on your computer.
1. Import [the CollectionBuilder CONTENTdm Skin repository](https://github.com/CollectionBuilder/collectionbuilder-cdm) into your own GitHub repository.
2. Pull down the repository/folder and open it using Visual Studio Code (or Atom) on your desktop.
2. Download and consult the [Metadata Template](https://docs.google.com/spreadsheets/d/1Uv9ytll0hysMOH1j-VL1lZx6PWvc1zf3L35sK_4IuzI/edit#gid=0).
3. Extract your own metadata from CONTENTdm using the Export Feature on the Collections Tab in the Administration portal. It can be found here: https://YOUR_SERVER_NUMBER.contentdm.oclc.org/cgi-bin/admin/exporth.exe?CISODB=/ui_ep
  - Use the "Tab-delimited" option and make sure the "Return field names in first record" option is clicked.
5. Upload that file into a Google Sheet
6. Follow the formatting of the example record in the template and adjust your own metadata accordingly.
  - Your metadata file and our example need not match up one-to-one, but certain fields, like "format," do need to follow certain standards. See [our Metadata Page]({{'/metadata/' | relative_url}}) for more details.
7. Save your metadata as a CSV file into the _data directory of your repository. 
8. Edit the _config.yml file to include your CONTENTdm server link and the directory details for where your collection ultimately ends up.  
9. Edit the theme.yml file found in the _data directory to reflect your specific collection details, including, most importantly, the name of the CSV file containing your metadata and the CONTENTdm id for your collection. 
10. Open up the terminal in your directory and write 'jekyll s' to serve up your website. 
11. Check your website and use the theme.yml file and the other "-config.csv" files in the _data directory to adjust the pages, layouts, and metadata displayed. 
12. When satisfied, stop your jekyll server by clicking 'CTRL + c' in the terminal, the write 'rake deploy' to build the site. 
13. Open up the _site folder, copy all the relevant HTML and css files, then paste these onto your web server. 
14. Your Web Site is up!

Coming Soon