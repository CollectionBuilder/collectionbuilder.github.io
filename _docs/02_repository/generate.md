---
title: Generating Your Site
stub: generate
section: repository
section_order: 4
---

{:.cdm .sa .typefilter}
{:.py-4 .mt-4 #generate}
***

{:.cdm .sa .typefilter}
## 6. Generating Your Site

{:.cdm .sa .typefilter}
Let's test the new code. Depending on the type of CollectionBuilder your using, there are two ways to generate the site. **GH** users will just need to turn on the GitHub Pages option via the settings page of their repository on GitHub.com. **SA** and **SKIN** users will want to use a jekyll command. Both approaches are listed below. 

{:.alert .alert-info}
NOTE: GitHub Pages will note work for **SA** and **SKIN** users, but **GH** users can use their local computer (if they've installed all the software) to serve their files in the same way that **SA** and **SKIN** users can." %}



{% capture serve-cdm-sa %}
Open the repository folder in your chosen text editor.
Editors like VS Code or Atom open the full folder making it easier work on the files as a group and provide tools such as an integrated terminal. 
(GitHub Desktop has a short cut "Open in text editor" available in the top bar)

1. If the terminal section of VSCode is not open, use the keyboard shortcut Ctrl + \` &nbsp; (control + backtick) to open it. 
2. In the terminal, type the command `jekyll s` and press enter. This "jekyll serve" command will generate the site for you on a local server on your computer. 
3. In the terminal you'll see some text appear, including a URL that appears after the title "Server address:"
4. Hold down `Ctrl`/`Cmd` and click this link to open the site in your browser. (Or highlight the url and `Shift + Ctrl + C`)
5. The generated site will be the demo version of CollectionBuilder. We'll show you soon how to add your own content soon!
6. When you're ready to end your jekyll session, simply type `Ctrl + C` into the terminal. This stops the server from running.
{% endcapture %}

{:.col-md-6}
{% include bootstrap/card.md text=serve-cdm-sa header="For SA and SKIN users" %}

{% capture serve-gh %}
Open the Seetings
Editors like VS Code or Atom open the full folder making it easier work on the files as a group and provide tools such as an integrated terminal. 
(GitHub Desktop has a short cut "Open in text editor" available in the top bar)

1. Go to the settings button at the top right of your repository page
2. Scroll down to the “GitHub Pages” section 
3. Change source dropdown button from “none” to “master” and copy the URL they give you.
4. It will take a couple minutes for the new website to build the first time, while your waiting go back to the main page and click the “edit” button on your repository page
5. Add the copied url to the website section and click “save" -- This will let you easily access the generated site whenever you come to edit the page.
6. Check out your new site by clicking on the link. Refresh if nothing shows up. Congratulations on setting up your own oral history site!
5. The generated site will be the demo version of CollectionBuilder. We'll show you soon how to add your own content soon!
{% endcapture %}

{:.col-md-6}
{% include bootstrap/card.md text=serve-gh header="For GH users" %}