
***So ... Where are the files???!!!***

One of the strange things about developing in this way is that while Jekyll is creating html files like its 1999, knowing where those files are and how to put them somewhere else is difficult to figure out. Let's lift the veil: 

**Jekyll builds the website in a directory called "_site."**

While generating the files for development--so when you are looking at the site after entering `jekyll s` in the commandline, the links it creates are based on that development server. But you'll also need one more command to build the site for production. Typically, that comand is "jekyll build," but we've added a few extra tasks to include analytics in a separate command called `rake deploy`.

{:.py-4 .mt-4 #rake-deploy}
***
### the 'rake deploy' command

When you're all finished, go to the terminal in VS Code and click 'CTRL C' to stop your development server. Then, write 'rake deploy' and push enter. This does two things: 

1. It builds the site with the appropriate (full) links 
    - (so www.lib.uidaho.edu/digital/boxing/browse.html rather than http://127.0.0.1:4000/digital/boxing/browse.hml)
2. It adds Google Analytics code based on the variable you added in the _config.yml file. 
    - This makes it so you don't have false hits on your analytics account.

If you didn't add analytics, that's fine too. It will build your site just the same as `jekyll build` does.

{:.py-4 .mt-4 #move-files}
***

### Moving the _site Files to Your Web Server

One you've completed the build process, the web files you need will all be in your _site director. Open that directory using your file explorer, copy everything, and then paste it into the directory on your web server you'd like to serve this site from. 

If you'd like to serve this up from a GitHub Pages enabled repository, that also could be doable. Talk to us. 


<hr class="my-4" />
<hr class="my-4" />

<div class="alert-warning p-4">
{%capture noteonjekyll %}
#### Note on Jekyll

Jekyll will work its Jekyll/Liquid/Markdown magic on any file in a folder that starts with an underscore ('_') or any file that starts with a YML portion, which starts on the first line with a "---" and ends after the assigned metadata (or no assigned metadata) with another line reading "---"

I'll provide this page's YML as an example:

{:.ml-4}
    `---`
    `title: Deploying the Collection`
    `step: 8`
    `---`

Then everything I'm writing here is below that. 

Jekyll uses that metadata to create the page, or any of the other commands you might need. 
{%endcapture%}
{{noteonjekyll | markdownify}}
</div>