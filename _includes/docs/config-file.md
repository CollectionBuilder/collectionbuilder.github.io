{%if page.collection == "contentdm" or page.collection == "workshop" %}Our CONTENTdm skin usese the CONTENTdm API to generate images, pdfs, and other downloadable files, but the metadata CSV file controls what appears on the pages. So after you have your config set up for your CONTENTdm instance and the collection, you can focus on improving your metadata to improve the site. 
{%endif%}
The **_config.yml** file connects your collection to the tool. The URL variables and the site settings section create that connection. So let's begin there. 

- [URL Variables](#url-var)
- [Repository Variables](#repo-var)
- [Site Settings](#site-settings)
- [Item Page Generation Settings](#page-gen)

{:.py-4 .mt-4}
***<a id="url-var"></a>

## URL Variables

These variables need to be defined based on where you expect the site to end up later. 

- **url** - If your project will be going up on a GitHub-Pages page, the url would look something like: "https://dcnb.github.io For the UI Library, we always use:  https://www.lib.uidaho.edu. This url represents the url where the site will ***eventually*** reside. It will be used to generate links when you build the site at the end of your customization process. 
    - example --> url: https://www.lib.uidaho.edu
- **baseurl** - This variable sets up the directories/folders that the site will end up in on your web server. So, for example, if you have a project called "pink-poodle" that you plan to put in the "projects" folder on your website, you'd put "/projects/pink-poodle" down for this variable. For the UI Library, we use /digital/ + the collection abbreviation to host our individual collections. You will need to adjust this setting for each collection you build. 
    - example --> baseurl: /digital/boxing 


{%if page.collection == "contentdm" or page.collection == "workshop" %}
{:.py-4 .mt-4}
***<a id="repo-var"></a>

## Repository Variables (leave blank if self-contained)
These variables are determine the root url for your CONTENTdm server and the id of your collection on that server. 

- **cdm-url** - This should be the url for your CDM server. 
    - example --> cdm-url: https://cdm17254.contentdm.oclc.org
- **cdm-collection-id** - The name of your contentdm collection.    
    - example --> cdm-collection-id: boxing 

{%endif%}

{:.py-4 .mt-4}
***<a id="site-settings"></a>



## Site settings
These are the primary settings of the site. The metadata variable controls where the site generates all visualizations. 

- **title** - The title of your digital collection. This appears on the home page banner and on every other page's header as well. 
	- example --> title: Donald R. Theophilus Boxing Photograph Collection
- **metadata** - the filename (not including the extension) of your CSV metadata file. Check against cdm-collection-id below -- the tool works better if these are the same. ***This should be the same entry as "data" in the page gen variables below.***
	- example --> title: boxing

{:.py-4 .mt-4}
***<a id="page-gen"></a>

## Item Page Generator Settings 
The pages for items are built when Jekyll builds the collection through the use of a ruby gem that you can find here: <https://github.com/avillafiorita/jekyll-datapage_gen>. This Gem reads your metadata file and builds individual html pages based on that data. 

There are several variables in this section. Most of them you should leave the same unless you want to do more extensive customization. The "data" variable, however, will need to be changed for each new collection: 

- **data** - This variable refers to the name of your metadata file, so it's really important. This should be changed for every collection to reflect the new file you are using. ***This should be the same entry as "metadata" above***
- **template** - This refers to the layout that you'd like to define your page. So, for CollectionBuilder, this is called "items."
- **name:** This deterimines how the URL will be written. For CollectionBuilder, we make this one 'object-id' because that is the field that we like to generate the URL. So, for the item with the object-id "boxing22," page-gen will create a url that ends "boxing22.html"
- **dir** This variable determines the directory or folder into which the item pages are stored. For CollectionBuilder, we use the directory "items."
- **extension** This deterimines the extension of each generated page. So, for us, 'html' means our item pages will end as '.html' 

##### example
	page_gen:
	  - data: 'boxing'
	    template: 'items'
	    name: 'object-id'
	    dir: 'items'
	    extension: 'html'   

{:.py-4 .mt-4}
***

## Additonal Variables

These are Git and Liquid based variable to help with building the site and recording the changes via git. You should probably just leave them as they are. The "profile' field allows liquid to determine bottlenecks via a commandline command. 'exclude' tells git which files and folders not to track when tracking the changes. And the 'sass' section controls how the CSS is build when the site is being rendered. 

##### example
	profile: true
	
    exclude: [docs/, Rakefile, README.md, LICENSE]

	## compress CSS output
	sass:
	 style: compressed

{:.py-4 .mt-4}
***