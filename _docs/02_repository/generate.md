---
title: Generate Your Site
stub: generate
section: repository
section_order: 4
---

{:.py-4 .mt-4 #generate}
***

## 4. Generating Your Site on a Test Server

Let's test the new code. 

Open the repository folder in your chosen text editor.
Editors like VS Code or Atom open the full repository folder making it easier work on the files as a group and provide tools such as an integrated terminal. 
(GitHub Desktop has a short cut "Open in text editor" available in the top bar)

1. If the terminal section of VSCode is not open, use the keyboard shortcut ``Ctrl + ` `` (control + backtick " **\`** ", the key left of "1" shared with "~") to open it. Or click the View menu at the top of VS Code and scroll down to "Terminal."
2. The **first time** you use this project folder on this computer, type the command: `bundle install`. Bundler will check the project's "Gemfile", install any missing dependencies, and create a "Gemfile.lock" listing the exact Gems set up for this project. You will see a bunch of output in your terminal window and if this is the first time bundling it may take awhile to finish.
Once complete your terminal prompt will return.
2. Next, in the terminal, type the command `bundle exec jekyll s` and press enter. This "jekyll serve" command will generate the site for you on a local server on your computer. 
3. In the terminal you'll see some text appear, including a URL that appears after the title "Server address:"
4. Hold down `Ctrl` and click this link to open the site in your browser (or copy the URL and paste into a private window).
5. The generated site will be the demo version of CollectionBuilder. We'll show you soon how to add your own content soon!
6. When you're ready to end your jekyll session, simply type `Ctrl + C` into the terminal. This stops the server from running.
