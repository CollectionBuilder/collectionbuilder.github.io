_config.yml Variables 


## URL Variables

These variables need to be defined based on where you expect the site to end up later. 

- **url** - If your project will be going up on a GitHub-Pages page, the url would look something like: "https://dcnb.github.io For the UI Library, we always use:  https://www.lib.uidaho.edu
    - example --> url: https://www.lib.uidaho.edu
- **baseurl** - This variable sets up the directories that the site will end up in. So if you have a project called pink-poodle that you want on in your projects folder on your website, you'd write "/projects/pink-poodle." For the UI Library, we use /digital/ + the collection abbreviation to host our indivdiual collections. So for each collection, we adjust this setting to reflect that. 
    - example --> baseurl: /digital/boxing 
- **digital-assets** - This is the url to a shared assets folder. We use "https://www.lib.uidaho.edu/assets." We've also made one avaiable here: "". You should probably just use that one, unless you'd like to copy ours and set one up on your own server. If you do that, just put the link to that folder in this variable. 
  - example --> digital-assets: https://www.lib.uidaho.edu/assets

## page gen settings 
The page gen settings use a ruby gem that you can find here: <https://github.com/avillafiorita/jekyll-datapage_gen>	. This Gem reads your metadata file and builds individual html pages based on that data. 

#### 'page_gen:'
There are several variables in this section. Most of them you should leave the same unless you want to do more extensive customization. The "data" variable, however, will be changed for each new collection: 

- **data** - This variable refers to the name of your metadata file, so it's really important. This should be changed for every collection to reflect the new file you are using. 
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

## Additonal Variables

These are git and liquid based variable to help with building the site and recording the changes via git. You should probably just leave them as they are. The "profile' field allows liquid to determine bottlenecks via a commandline command. 'exclude' tells git which files and folders not to track when tracking the changes. And the 'sass' section controls how the CSS is build when the site is being rendered. 

##### example
	profile: true
	
    exclude: [docs/, Rakefile, README.md, LICENSE]

	## compress CSS output
	sass:
	 style: compressed
