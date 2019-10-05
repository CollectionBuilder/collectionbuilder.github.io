

We will ask below that you check if you're computers have the software we'd like you to install. To do this, you'll need to open the terminal/command line and type something like "ruby -v" and push enter. We know the command line is something that keeps many of us from using certain software, but we're hoping you'll trust us and push on! 

So the question remains, *How do I get into the command line?*

Both Mac and Windows users should be able to type "terminal" into their respective system search bars--Mac's is at the top right and Windows' is at the bottom right.  This will open the terminal for you so you can run the 'ruby -v' type checks below. 

Alternatively, the text editors we recommend will also allow you to use the terminal from whatever directory you have. This is super handy. And it's good practice for building sites later, so you might use this method to build familiarity.

### Quickly get into the command line using VS Code

- If you're not familiar with the command line, and you've just installed Visual Studio Code, go ahead and open up the software. 
- Mouse to the menu at the top of the program (with "File", "Edit", etc. ) and select "View". 
- Scroll down to where it says "Terminal" and click the word. 
  -(Alternatively, you can hit CTRL and ~ at the same time, which is a good shortcut to remember.)
- This will open up a terminal, also known as the command line, in the folder you are working in. So, if you just opened it up without opening a file or a folder, it will likely be open on the Desktop. 
- Later on, you will want to use VS Code to open up your CollectionBuilder folder, and then open up the terminal from there, so you can run the site on your own computer (but that's getting ahead of ourselves!)

### The only two commands you need to use in the command line

Once your environment is set up, you'll be using two main commands in building your digital collections: 

1. "jekyll s" 
  - This will 'serve' the web site up using your computer as the web server so you can check the various pages before building the site
2. "rake deploy"
  - This will build your site, building in certain features like analytics that you wouldn't want running while you are developing. After running this command, you're full website is built in the '_site' folder. 