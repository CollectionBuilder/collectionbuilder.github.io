---
title: Clone Your Repository
stub: clone
section: repository
section_order: 2
---

{:.py-4 .mt-4 #clone}
***

{:.alert .alert-warning}
**For GH users** The rest of the instructions on this page are optional for you. You can move on to the [metadata](metadata.html) section. GH was designed so that all the edits can be made through the web interface. <br><br>If you'd like to work on your repository on your local computer, and you've [installed](software.html) all the software required), you can follow the below and work in the same way as the other types.   

## 2. Clone Your New Repository to Your Local Machine

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
