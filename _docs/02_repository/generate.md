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
Let's test the new code. 
Open the repository folder in your chosen text editor.
Editors like VS Code or Atom open the full folder making it easier work on the files as a group and provide tools such as an integrated terminal. 
(GitHub Desktop has a short cut "Open in text editor" available in the top bar)

{% capture serve %}
1. If the terminal section of VSCode is not open, use the keyboard shortcut Ctrl + \` &nbsp; (control + backtick) to open it. 
2. In the terminal, type the command `jekyll s` and press enter. This "jekyll serve" command will generate the site for you on a local server on your computer. 
3. In the terminal you'll see some text appear, including a URL that appears after the title "Server address:"
4. Hold down `Ctrl`/`Cmd` and click this link to open the site in your browser. (Or highlight the url and `Shift + Ctrl + C`)
5. The generated site will be the demo version of CollectionBuilder. We'll show you soon how to add your own content soon!
6. When you're ready to end your jekyll session, simply type `Ctrl + C` into the terminal. This stops the server from running.
{% endcapture %}
{:.cdm .sa .typefilter}
{% include bootstrap/card.md text=serve %}

{:.cdm .sa .typefilter}
Let's take a few minutes to walk through how Jekyll generates this website from the demo metadata by pulling together template parts.
