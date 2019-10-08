---
title: Software Installation and Set Up
step: 1
---

If you're working with CollectionBuilder-gh, you don't have to worry about an environment, as everything can be done through GitHub's web interfaces. That said, it's much easier, once everything is set up, to work on a computer set up for developing with these tools. 

Getting the software installed on your computer is typically the biggest hurdle to getting started with tools like ours. So stick with it, even if you run into any issues. Jeykll requires Ruby, and the workflows we use include the use of Git and GitHub. And working in these repositories will also require a text editor, so let's get that first: 

## 1. Get a Text Editor

When working with code you should have a good text editor.
Word processors such as MS Word can not be used to create or edit code; they add all sorts of gunk to the text.
Windows Notepad does not handle UTF-8 encoding or UNIX line endings that are standard for cross platform applications. 

For basic editing, Windows [Notepad++](https://notepad-plus-plus.org/), Mac TextEdit, or Linux Gedit are sufficient.
However, a more complete code editor is recommended for managing Jekyll projects.

Open-source cross platform suggestions:

- [Visual Studio Code](https://code.visualstudio.com/) (VS Code) - we recommend this program, especially if you're new to the command line. 
- [Atom](https://atom.io/)

If you don't have one of these text editors installed, visit their sites, download the software, and use their wizards to install the software on your computer. We mostly use Visual Studio Code, so if you don't know which one to pick, go ahead and get that one. 

>*Note: For installation, especially on a Mac, we ask that you check and see if you have certain versions of the software already. If you're new or nervous about using the command line / terminal, check out our page on it here: <https://collectionbuilder.github.io/skins/contentdm/docs/commandline.html>. *

## 2. Install Git

[Git](https://git-scm.com/) is a [free](https://www.gnu.org/philosophy/free-sw.en.html), [distributed](https://en.wikipedia.org/wiki/Distributed_version_control) version control system, a piece of software on your computer. 
[GitHub](https://github.com/) is a Git repository hosting service, a place to store and sync your work in the cloud.
Your GitHub Pages projects will be under Git version control, so you need the software on your machine. 

Installing it is fairly straightforward:

- **Windows:** install [Git for Windows](https://git-for-windows.github.io/){:target="_blank"} using the default options, except when setup asks you to choose the default editor used by Git, select "Use the Nano editor by default". This will give you Git, Git Bash, and Git GUI. Git Bash is a great terminal that lets you use UNIX style commands and utilities on Windows.
- **Mac:** check if Git is already installed by opening terminal and typing `git --version`. If you do not have it, your system will often prompt you to install "Xcode Command Line Tools"--follow the prompt as this package is necessary for Ruby as well. Alternatively, type `xcode-select --install` to start the process. If you want a newer version, download the official [Mac git installer](https://git-scm.com/downloads){:target="_blank"} or use Homebrew.
- **Linux:** install from your distribution's software center or package manager (for Ubuntu `sudo apt install git`).

IF you are new to using Git and GitHub, we'd also recommend you install [GitHub Desktop](https://desktop.github.com/){:target="_blank"} using the default options. This will help you visualize and implement some of the git processes that often seem non-intuitive. You can install GitHub Desktop in addition to other versions of Git.

Note: If you are a Linux user, GitHub Desktop will not work. There are, however, other [GUI apps available](https://git-scm.com/downloads/guis){:target="_blank"} for managing and visualizing Git repositories, including Linux options.

## 3. Install Ruby

[Ruby](https://www.ruby-lang.org/en/){:target="_blank"} is a fairly young and developing programming language with some unique features. 
To use Jekyll, ***you do not need to know anything about Ruby***, but if you are curious, check out [Ruby in 20 minutes](https://www.ruby-lang.org/en/documentation/quickstart/){:target="_blank"}.

Frustratingly, different versions have many dependency and incompatibility problems.
Because of these issues, many use Ruby Managers, such as [RVM](http://rvm.io/){:target="_blank"}, to install and switch between versions.
However, if you are just interested in working with Jekyll, using an installer for your OS should work well.
Jekyll requires a Ruby version that is greater than 2.2.5.

- **Windows:** Use [RubyInstaller for Windows](https://rubyinstaller.org/){:target="_blank"}. 
    - First, [download](https://rubyinstaller.org/downloads/){:target="_blank"} the suggested stable version "WITH DEVKIT" (as of this writing, Ruby+Devkit 2.5.X (x64)) and double click to install. Use the install defaults, but make sure "Add Ruby executables to your PATH" is checked. On the final step, ensure the box to start the MSYS2 DevKit is checked.
    - Second, the installer will open a terminal window with options to install MSYS2 DevKit components. Choose option 3, "MSYS2 and MINGW development toolchain", or simply press ENTER to install all the necessary dependencies. The installer will proceed through a bunch of steps outputting a bunch of text in the terminal window--*eventually*, this will conclude and you should see a message with success in it. If the window doesn't close, press Enter again or manually close it. (The installer can be restarted by typing `ridk install` into a command prompt)
- **Mac:** OS X has a version of Ruby installed by default. Check the version with `ruby -v`. If it is > 2.2.5 you can use the system Ruby, but recommended practice is to set up a separate Ruby development environment. To do this, follow the instructions below, which outline the steps to install Ruby using [Ruby Version Manager (RVM)](https://rvm.io/){:target="_blank"}. Alternatively, some people have success using [Homebrew](https://brew.sh/){:target="_blank"} (`brew install ruby`) or another manager such as [rbenv](https://github.com/rbenv/rbenv){:target="_blank"}, but our experience suggests RVM is best option.
    - Ensure you have Xcode Command Line Tools, if not use `xcode-select --install` to start the installer.
    - Install [Ruby Version Manager (RVM)](https://rvm.io/){:target="_blank"} following the steps below:
        - Install gpg2, using [Homebrew](https://brew.sh/){:target="_blank"}: `brew install gnupg`
        - Get the public key from [https://rvm.io/rvm/install](https://rvm.io/rvm/install){:target="_blank"}: `gpg --keyserver hkp://pool.sks-keyservers.net --recv-keys 409B6B1796C275462A1703113804BB82D39DC0E3 7D2BAF1CF37B13E2069D6956105BD0E739499BDB`
        - Get the helper script and install RVM stable with ruby: `\curl -sSL https://get.rvm.io | bash -s stable --ruby`
    - Install recent stable version of Ruby:
        - Check [Ruby Downloads](https://www.ruby-lang.org/en/downloads/){:target="_blank"} for number of "current stable version", currently 2.6.4
        - Use RVM to install that version: `rvm install 2.6.4` (this may take a long time...)
        - Set it as default Ruby: `rvm --default use 2.6.4`
        - Check: `ruby -v`
- **Linux:** Even though the version will not be the most up-to-date, the simplest method is to use your distro's repositories. For example on Ubuntu, `sudo apt install ruby-full`. Check `ruby -v` to make sure the repository version is > 2.2.5. See the official Jekyll [Ubuntu install docs](https://jekyllrb.com/docs/installation/ubuntu/){:target="_blank"} for more details.
    - For a more up-to-date version, use a manager such as [RVM](http://rvm.io/){:target="_blank"} ([Ubuntu tips](https://evanwill.github.io/_drafts/notes/ruby-notes.html){:target="_blank"})
    - You will also need some build tools (Make and GCC), on Ubuntu get them with `sudo apt install build-essential`.

## 4. Install Jekyll

Jekyll is a Gem, a software package installed via Ruby's management system called RubyGems (similar to Python's Pip). 
Open a terminal and type:

`gem install jekyll bundler`

This will take a minute as Gem installs all the dependencies and builds extensions (on Windows it may appear as if nothing is happening, but be patient!). 

> Note: Linux users may need to `sudo`, to avoid this install Ruby using [RVM](http://rvm.io/) or add a gem install directory to `.bashrc`.
> On Windows, if `gem` returns an error about secure connections, it may be necessary to update to a newer version of RubyGems as some versions have out of date SSL certificates.
> Manually install the newer version by downloading the [RubyGems zip package](https://rubygems.org/pages/download#formats).
> Unzip the package, then run `ruby setup.rb` in the directory.

> Note: Jekyll does not officially support Windows, however it works fine on Windows (they just don’t officially write windows documentation or check for bugs). 
> There is a [Jekyll on Windows](https://jekyllrb.com/docs/installation/windows/) page, but it can be out of date and inaccurate.