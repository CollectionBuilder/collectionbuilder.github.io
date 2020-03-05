---
title: Install Git and GitHub Desktop
stub: git
section: software
section_order: 2
---

{:.py-4 .mt-4 #git}
***

## 2. Install Git and GitHub Desktop

To manage the code and collaborate on developing your CollectionBuilder project, you need a version control system to keep everything organized. 

[GitHub](https://github.com/){:target="_blank" rel="noopener"} is a cloud [Git](https://git-scm.com/){:target="_blank" rel="noopener"} repository hosting service with features for collaboration and project management.
Think of it as Google Drive for code with super robust "track changes" baked in.

GitHub is the most popular platform for developing and sharing code -- from enterprise software, to hands-on learning, to academic projects.
Thus, it is great to become familiar with the platform so that you can take part in this community.

Code for your CollectionBuilder project will be stored on GitHub. 
To connect locally, you'll need to install Git (the version control software that powers GitHub) and GitHub Desktop (a handy visual way to use Git) on your local computer.

{% capture git %}
- **Windows:** 
    - Install [Git for Windows](https://git-scm.com/downloads){:target="_blank" rel="noopener"} using the default options, *except* when setup asks you to choose the default editor used by Git, select "Use the Nano editor by default". This will give you Git, Git Bash, and Git GUI. Git Bash is a terminal that lets you use UNIX style commands and utilities on Windows, and will be used as your default terminal when working with Jekyll.
- **Mac:** 
    - Mac systems will require the "Xcode Command Line Tools" installed, so open a terminal (to find your terminal search for "terminal" in your Spotlight), type in the command `xcode-select --install`, and follow the prompts. After the install finishes, try typing `git --version`. If you want a newer version of Git, download the official [Mac git installer](https://git-scm.com/downloads){:target="_blank" rel="noopener"}.
- **Linux:** 
    - Install from your distribution's software center or package manager (for Ubuntu `sudo apt install git`).
{% endcapture %}
{% include bootstrap/card.md text=git header="Install Git" %}

{% capture gitconfig %}
Once Git is installed, we need to configure your information, so that it can connect with your GitHub account.
Since Git is a command line application, we will need to open a terminal to give it commands. 
On Windows, search for "Git Bash."
On Mac and Linux, search for "terminal."
Once you have a terminal open, we will need to give it two commands.

First, set your user name so that it matches your GitHub user name:

`git config --global user.name "User Name"`

Second, set your email so that it matches your GitHub email:

`git config --global user.email "myemail@gmail.com"`

{% capture commit %}
Your email and user name is recorded with every commit.
This helps ensure integrity and authenticity of the history.
Most people keep their email public. However, if you are concerned about privacy, check GitHub's tips on how to [set up your email](https://help.github.com/en/github/setting-up-and-managing-your-github-user-account/setting-your-commit-email-address#about-commit-email-addresses){:target="_blank" rel="noopener"}. GitHub now provides a no-reply email address that can be accessed via your email settings on GitHub.com.
{% endcapture %}
{% include bootstrap/alert.md text=commit color="info" %} 
{% endcapture %}
{% include bootstrap/card.md text=gitconfig header="Configure Git" %}

{% capture gitdesk %}
If you are new to using Git and GitHub, we also recommend you install [GitHub Desktop](https://desktop.github.com/){:target="_blank" rel="noopener"} using the default options. 
This will help you visualize and implement some of the git processes that often seem non-intuitive.
{% endcapture %}
{% include bootstrap/card.md text=gitdesk header="Install GitHub Desktop" %} 
