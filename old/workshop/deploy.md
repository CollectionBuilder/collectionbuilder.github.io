
***So ... Where are the files???!!!***

One of the strange things about developing in this way is that while Jekyll is creating html files like its 1999, knowing where those files are and how to put them somewhere else is difficult to figure out. Let's lift the veil: 

**Jekyll builds the website in a directory called "_site."**

While generating the files for development--so when you are looking at the site after entering `jekyll s` in the commandline, the links it creates are based on that development server. But you'll also need one more command to build the site for production. Typically, that comand is "jekyll build," but we've added a few extra tasks to include analytics in a separate command called `rake deploy`.

1. [Building the Site](#rake-deploy)
2. [Moving the _site Files to Your Web Server](#move-files)

{:.py-4 .mt-4 #rake-deploy}
***
### 1. Building the Site ("rake deploy")

When you are all finished, go to the terminal in VS Code and click 'CTRL C' to stop your development server. Then, write 'rake deploy' and push enter. This does two things: 

1. It builds the site with the appropriate (full) links 
    - (so www.lib.uidaho.edu/digital/boxing/browse.html rather than http://127.0.0.1:4000/digital/boxing/browse.html)
2. It adds Google Analytics code based on the variable you added in the [_config.yml file](config.html). 
    - This prevents false hits on your analytics account.

If you didn't add analytics, that's fine too. It will build your site just the same as `jekyll build` does.

{% include bootstrap/alert.md color="warning" text="#### A Note on Google Analytics

We don't necessarily recommend adding Google Analytics to your website. Last year, we actually deleted analytics from our catalog due to patron privacy concerns related to Google's agrressive tracking of users online. 

We do assume, however, a large number of our eventual users might use the tool to collect web statistics (we do on our other sites). 

If you're interested in an analytics tool that doesn't track your users, we've enjoyed looking at Matomo recently. We haven't added a Matomo option but we might add that or another analytics tool in the future."  %}

{:.py-4 .mt-4 #move-files}
***

### 2. Moving the _site Files to Your Web Server

One you've completed the build process, the web files you need will all be in your "_site" directory. 

1. Open that directory using your file explorer or finder.
2. Copy everything you'd like to move into a production site.
3. Paste those files and folders into the directory on your web server you'd like to serve this site from. 

*Note: If you'd like to serve this up from a GitHub Pages enabled repository, that also could be doable. Talk to us.*

{% include bootstrap/alert.md color="success" text="That's it. You've Done It. And hopefully now you can do it again (and again and again), and after awhile, teach others this development model and/or tool as well. (Let us know if we can help!)" %}


<hr class="my-4" />
<hr class="my-4" />

<!--<div class="alert-warning p-4">
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
</div>-->