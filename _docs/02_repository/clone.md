---
title: Clone Your New Repository to Your Local Machine
stub: clone
section: repository
section_order: 2
---

{:.py-4 .mt-4 #clone}
***

## 2. Clone Your New Repository to Your Local Machine

{:.alert .alert-info}
**For GH users** This is an optional method of working on your repository. You can install Git and GitHub Destkop on your computer (+ a text editor) and edit your files via your local system, if you'd like. But GH was designed so that all the edits can be made through the web interface. 

Now that you have a repository set up on GitHub, we need to copy that folder down to your local machine. 
*Cloning* the repository ensures the local version on your laptop is automatically configured to be connected to the version on GitHub.

{% capture clone %}
1. On your new repository page, click on the green button in the upper right labeled "Clone or download."
2. In the box that pops up, click on the button labeled "Open in Desktop." 
    - This action will automatically open GitHub Desktop for you. 
    - GitHub Desktop will ask you to confirm the path of the repository you are cloning to your computer. In most cases, the path that it suggests is fine to use so you can just click on the blue "Clone" button.
{% endcapture %}
{% include bootstrap/card.md text=clone %}

GitHub Desktop *clones* your repository by downloading a complete copy of the code and history from GitHub and storing it in a folder on your computer.
It is important to realize that the repository really is just a folder of files!
You can open, move, or edit it just like any other folder on your computer.

Now, in the top bar of GitHub Desktop you should see three buttons. 
On the left, the "Current repository" button lists the repository  you just cloned. 
In the middle, you can check your current branch (it should say *master*), and on the right there is a button that allows you to "**Fetch origin**," "**Pull origin**," or "**Push origin**." 
As you work, this button allows you to sync the local version of your repository with the version on GitHub, and push and pull changes between them.
