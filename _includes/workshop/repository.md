
Now that your *development environment* is ready to go, we need to get the code and set up a CollectionBuilder project.

1. [Download CB Release](#download)
2. [Create a Repository](#create)
3. [Clone Your New Repository](#clone)
4. [Add CB Files](#add)
5. [Committing and Pushing Your New Files](#commit)
6. [Generating Your Site](#generate)
7. [Editing Your Repository](#edit)


{:.py-4 .mt-4 #download}
***

## 1. Download the Latest CollectionBuilder Release

First, you need to get a copy of the CollectionBuilder code.
You can always find the latest "stable" code on our [Release Page](https://github.com/CollectionBuilder/collectionbuilder-contentdm/releases) and download the `Source code (zip)` folder.
The main [CollectionBuilder-CONTENTdm](https://github.com/CollectionBuilder/collectionbuilder-contentdm) repository is where active development is taking place, so choosing a release will ensure the project is fully functional.
Click here to download our latest release:

{% include bootstrap/button.md text="CollectionBuilder-CONTENTdm v1.02" link="https://github.com/CollectionBuilder/collectionbuilder-contentdm/archive/v1.02.zip" color="success" %}

{:.py-4 .mt-4 #create}
***

## 2. Create a New Repository

Second, you need to set up a repository on GitHub for your CollectionBuilder project.
Each repository on GitHub is basically a folder for storing and tracking the code for a project.

{% capture newrepo %}
1. Login on [GitHub](https://github.com)
2. In the top right corner, click the *plus* icon and select "New Repository"
3. This brings you to a "Create a new repository" form. Follow these steps:
    - **Enter your new repository name**. It is best to use a naming convention without spaces or odd characters. We often append `_source` or `_draft` to our projects to keep track of the status. 
    - Check the box next to "**Initialize this repository with a README**"
    - Click on the button that says "**Add .gitignore:**" and in the filter type `jekyll`. When **Jekyll** appears as an option, click on it.
    - Click on the green button "**Create repository**." This will take you to your new repository.
{% endcapture %}
{% include bootstrap/card.md text=newrepo %}

{:.py-4 .mt-4 #clone}
***

## 3. Clone Your New Repository

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

{:.py-4 .mt-4 #add}
***

## 4. Add CollectionBuilder Files

Add the CollectionBuilder code that you downloaded into the new repository: 

1. In the bar at the top of your GitHub Desktop window, click on "Repository," then click on "Open in Explorer" (if you're on a PC) or "Open in Finder" (if you're on a Mac). This will show you the location of the repository you just cloned to your computer
2. Open another Explorer/Finder window, and locate the `collectionbuilder-contentdm-1.0.zip` that you downloaded
3. Unzip `collectionbuilder-contentdm-1.0.zip` 
4. Navigate into the folder, copy (`Ctrl + A`, `Ctrl + C`) the contents and paste (`Ctrl + V`) into your new repository

{:.py-4 .mt-4 #commit}
***

## 5. Committing and Pushing Your New Files

Now, if you switch back to GitHub Desktop, you should see the files you just copied into the repository show up in the "Changes" column on the left side of the window.
This is Git alerting you that it noticed that something changed!
We can take a snapshot of those changes, storing them into the history of the repository by doing a Git *Commit*.

{% capture commit %}
On GitHub Desktop, below the list of changes, you'll see a text-entry box labeled "Summary (required)." 

- Type a "commit" message into the box -- a short message describing the changes you've made. In this case, you might enter something like "upload base collectionbuilder code." 
- When you've finished your commit message, click on the blue button toward the bottom of the column that says "Commit to master."
- The "Changes" disappear, you've just made a Git Commit!

Now you've committed your changes locally, but haven't pushed them to the online repository yet. 
To push your commit up to GitHub, click on the button at the top right of the GitHub desktop screen that says "Push changes."

- Click "Push changes"
- Navigate to your repository on GitHub web interface-- you'll see that it's been updated with the new files
- **Congratulations, you've pushed your first commit to GitHub!**
{% endcapture %}
{% include bootstrap/card.md text=commit header="Git Commit and Push" %}

{:.py-4 .mt-4 #generate}
***

## 6. Generating Your Site

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
{% include bootstrap/card.md text=serve %}

Let's take a few minutes to walk through how Jekyll generates this website from the demo metadata by pulling together template parts.

{:.py-4 .mt-4 #edit}
***

## 7. Editing Your Repository

Once you start **customizing your repository**, here are a few things you should know:

1. GitHub Destkop and your text editor (probably VSCode or Atom) are looking at the same folder of files (your repository), so once you save the changes you make to files in your text editor, those changes will show up in the left-hand "Changes" column in GitHub Desktop. 
    - When you're ready to commit the changes you've made, simply navigate to GitHub Desktop and select the checkboxes next to the files you'd like to commit. 
    - Enter your commit message in the box at the bottom of the column, click the blue "Commit to master" button, and push your changes using the button in the top right of the GitHub Desktop window.
2. If you're working on multiple computers or collaborating, be sure to fetch and pull changes before you push new ones. 
    - You can do this by clicking on the button in the top right of the GitHub Desktop interface labeled "**Fetch origin**." 
    - If there is content to pull, once it is fetched this button will say "**Pull origin**." Click on the button to pull the changes, and you will see your local repository change accordingly.
