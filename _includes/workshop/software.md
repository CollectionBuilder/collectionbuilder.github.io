Getting the software installed on your computer is typically the biggest hurdle to getting started with tools like CollectionBuilder. 
So stick with it, even if you run into issues. 
Having your local "development environment" for a Jekyll-based project set up will be rewarding, allowing you to edit code and see how the website changes right on your laptop.

To get started editing code, managing your project, and building websites with CollectionBuilder-CONTENTdm you will need: 

1. [Text Editor](#text-editor)
2. [Git](#git) (version control system)
3. [Ruby](#ruby) (programming language)
4. [Jekyll](#jekyll) (static web site generator)

This section will walk you through installing software and provide a brief overview how this *development environment* fits together.

{:.py-4 .mt-4 #text-editor}
***

## 1. Get a Text Editor

All code is [plain text](https://en.wikipedia.org/wiki/Plain_text), and all plain text can be edited by a "text editor." 
Word processors, such as MS Word, can not be used to create or edit code, as they  do not handle plain text without altering it.
For basic editing, Windows [Notepad++](https://notepad-plus-plus.org/), Mac TextEdit, or Linux Gedit are sufficient.
However, for a Jekyll project such as CollectionBuilder, a more complete code editor is recommended. 

The CollectionBuilder team suggests these open-source, cross platform options for text editors:

- [Visual Studio Code](https://code.visualstudio.com/) (VS Code)
- [Atom](https://atom.io/)

If you don't have one of these text editors installed, visit their sites, download the software, and use their wizards to install the software on your computer. 
We mostly use Visual Studio Code, so if you don't know which one to pick, go ahead and get that one. 
For additional assistance, see our guides for [How to Install and Set Up Visual Studio Code](https://lib-static.github.io/howto/howtos/visualstudiocode.html){:target="_blank"} and [How to Install and Set Up Atom](https://lib-static.github.io/howto/howtos/installatom.html){:target="_blank"}

{% capture vscode %}
When you first install VS Code, the default settings can be distracting. 
To configure the editor, click the *gear icon* in the bottom left corner of the VSCode window and choose *Settings*.
The searchable *Settings* pane has information about all the configuration options.

To make it easy to share settings, you can also paste values into your **settings.json** file which represents all the options customized on the *Settings* pane.
Click the *file icon* in the upper right of the *Settings* pane to view your configuration as JSON.
Copying and pasting the JSON snippet below into your settings will turn off some of the distraction. 

```
{
    "editor.minimap.enabled": false,
    "editor.wordWrap": "on",
    "html.format.maxPreserveNewLines": 2,
    "html.format.wrapLineLength": 0,
    "editor.codeLens": false,
    "outline.problems.badges": false,
    "outline.problems.enabled": false,
    "outline.problems.colors": false,
    "problems.decorations.enabled": false,
    "problems.autoReveal": false
}
```

Once you paste it in, save (`CTRL + S`) and close the **settings.json** file.
{% endcapture %}
{% include bootstrap/card.md text=vscode header="Configuring Visual Studio Code" %}

{:.py-4 .mt-4 #git}
***

## 2. Install Git and GitHub Desktop

To manage the code and collaborate on developing your CollectionBuilder project, you need a version control system to keep everything organized. 

[GitHub](https://github.com/) is a cloud [Git](https://git-scm.com/) repository hosting service with features for collaboration and project management.
Think of it as Google Drive for code with super robust "track changes" baked in.

GitHub is the most popular platform for developing and sharing code -- from enterprise software, to hands-on learning, to academic projects.
Thus, it is great to become familiar with the platform so that you can take part in this community.

Code for your CollectionBuilder project will be stored on GitHub. 
To connect locally, you'll need to install Git (the version control software that powers GitHub) and GitHub Desktop (a handy visual way to use Git) on your local computer.

{% capture git %}
- **Windows:** 
    - Install [Git for Windows](https://git-scm.com/downloads){:target="_blank"} using the default options, *except* when setup asks you to choose the default editor used by Git, select "Use the Nano editor by default". This will give you Git, Git Bash, and Git GUI. Git Bash is a terminal that lets you use UNIX style commands and utilities on Windows, and will be used as your default terminal when working with Jekyll.
- **Mac:** 
    - Mac systems will require the "Xcode Command Line Tools" installed, so open a terminal (search for "terminal" in your Spotlight), type in the command `xcode-select --install`, and follow the prompts. After the install finishes, try typing `git --version`. If you want a newer version of Git, download the official [Mac git installer](https://git-scm.com/downloads){:target="_blank"}.
- **Linux:** 
    - Install from your distribution's software center or package manager (for Ubuntu `sudo apt install git`).
{% endcapture %}
{% include bootstrap/card.md text=git header="Install Git" %}

{% capture gitconfig %}
Once Git is installed, we need to configure your information, so that it can connect with your GitHub account.
Since Git is a command line application, we will need to open a terminal to give it commands. 
On Windows, search for "Git Bash". 
On Mac and Linux, search for "terminal".
Once you have a terminal open, we will need to give it two commands.

First, set your user name so that it matches your GitHub user name:

`git config --global user.name "User Name"`

Second, set your email so that it matches your GitHub email:

`git config --global user.email "myemail@gmail.com"`

{% capture commit %}
Your email and user name is recorded with every commit.
This helps ensure integrity and authenticity of the history.
Most people keep their email public, however, if you are concerned about privacy, check GitHub's tips to [hide your email](https://help.github.com/articles/about-commit-email-addresses/){:target="_blank"}.
{% endcapture %}
{% include bootstrap/alert.md text=commit color="secondary" %} 
{% endcapture %}
{% include bootstrap/card.md text=gitconfig header="Configure Git" %}

{% capture gitdesk %}
If you are new to using Git and GitHub, we'd also recommend you install [GitHub Desktop](https://desktop.github.com/){:target="_blank"} using the default options. 
This will help you visualize and implement some of the git processes that often seem non-intuitive.
{% endcapture %}
{% include bootstrap/card.md text=gitdesk header="Install GitHub Desktop" %} 

{:.py-4 .mt-4 #ruby}
***

## 3. Install Ruby

[Ruby](https://www.ruby-lang.org/en/){:target="_blank"} is a programming language popular with web applications. 
**_You do not need to know anything about Ruby_**, but you do need it to run Jekyll on your system!

Jekyll requires a Ruby version that is greater than 2.4.0.

{% capture win-ruby %}
Use [RubyInstaller for Windows](https://rubyinstaller.org/){:target="_blank"}. 

- First, [download](https://rubyinstaller.org/downloads/){:target="_blank"} the suggested stable version "WITH DEVKIT" (as of this writing, Ruby+Devkit 2.6.X (x64)) and double click to install. Use the install defaults, but make sure "Add Ruby executables to your PATH" is checked. On the final step, ensure the box to start the MSYS2 DevKit is checked.
- Second, the installer will open a terminal window with options to install MSYS2 DevKit components. Choose option 3, "MSYS2 and MINGW development toolchain", or simply press ENTER to install all the necessary dependencies. The installer will proceed through a bunch of steps outputting a bunch of text in the terminal window -- *eventually*, this will conclude and you should see a message with success in it. If the window doesn't close, press Enter again or manually close it. (The installer can be restarted by typing `ridk install` into a command prompt)
- Having trouble? Need more detail? See [How to Install Ruby on Windows](https://lib-static.github.io/howto/howtos/installrubywindows.html){:target="_blank"} for help.
{% endcapture %}
{% include bootstrap/card.md text=win-ruby header="Ruby on Windows" %}

{% capture mac-ruby %}
Installing Ruby on Mac can be difficult, but don't be deterred! If the method below doesn't work for you check out [How to Install Ruby on a Mac](https://lib-static.github.io/howto/howtos/installrubymac.html){:target="_blank"} for more detail and other options.

OS X has a version of Ruby installed by default, but recommended practice is to set up a separate Ruby development environment. 
To do this, follow the instructions below, which outline the steps to install Ruby using [Ruby Version Manager (RVM)](https://rvm.io/){:target="_blank"}. 
Alternatively, some people have success using [Homebrew](https://brew.sh/){:target="_blank"} or another manager such as [rbenv](https://github.com/rbenv/rbenv){:target="_blank"}, but our experience suggests RVM is best option.

- Ensure you have Xcode Command Line Tools, if not use `xcode-select --install` to start the installer.
- Ensure you have [Homebrew](https://brew.sh/){:target="_blank"} installed. The website provides an installer script that can be pasted into the terminal.
- Install [Ruby Version Manager (RVM)](https://rvm.io/){:target="_blank"} following the steps below:
    - Install gpg2, using Homebrew: `brew install gnupg`
    - Get the [public key from RVM](https://rvm.io/rvm/install){:target="_blank"}, by copying the command starting with `gpg` into your terminal.
    - Get the helper script and install RVM stable with ruby: `\curl -sSL https://get.rvm.io | bash -s stable --ruby`
    - Close terminal, reopen and type `rvm list`. If the lists shows the new Ruby set as default, you are all set. Otherwise, set the default Ruby using `rvm --default use` plus the version numbers (e.g. `2.6.3`).
    - Check your version with `ruby -v`
{% endcapture %}
{% include bootstrap/card.md text=mac-ruby header="Ruby on Mac" %}

{% capture ruby-lin %}
Ruby can be installed via most distro's repositories, however, it is more up-to-date and best practice to use a version manager such as [RVM](http://rvm.io/){:target="_blank"}.

- First, ensure you have build tools Make and GCC installed (on Ubuntu get them with `sudo apt install build-essential`)
- Follow the instructions on [RVM install](https://rvm.io/rvm/install){:target="_blank"}
{% endcapture %}
{% include bootstrap/card.md text=ruby-lin header="Ruby on Linux" %}

{:.py-4 .mt-4 #jekyll}
***

## 4. Install Jekyll

Finally, we get to [Jekyll](https://jekyllrb.com/)!
Jekyll is a static site generator that uses templates and data to build out websites. 
It is a very popular project used by tiny and giant projects. 

Jekyll is a Gem, a software package installed via Ruby's management system called RubyGems (similar to Python's Pip). 
Gem is a command line application, so again we will open a terminal to give it commands.
Once you have a terminal open, type in:

`gem install jekyll bundler`

{% include bootstrap/alert.md text="This will take awhile as Gem installs all the dependencies and builds extensions (on Windows it may appear as if nothing is happening, but be patient!)." color="warning" %}

Your dev environment is ready! Give yourself a hand!
