
Now that your software is ready to go, the following steps outline the workflow you'll use when you start working with GitHub and Git to create and edit your collection.

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

1. Log in to the [GitHub](https://github.com){:target="_blank"} web interface and go to our [collectionbuilder-contentdm](https://github.com/CollectionBuilder/collectionbuilder-contentdm){:target="_blank"} repository.
2. Navigate to the latest project release. You can do this by clicking on the "Releases" tab, which you'll find in the second navigation bar, below the row the "Code" tab is in. 
3. Download the `Source code (zip)` folder.

{:.py-4 .mt-4 #create}
***

## 2. Create a New Repository

1. Navigate back to your own GitHub account Repositories page.
2. In the top right corner, click on the green button labeled "New."
3. This brings you to a "Create a new repository" form. Follow these steps:
    - **Enter your new repository name**, and give your project a **description**. 
        - If you have a free account you will have to make the respository public, but if you have a paid account or are part of an organization, you can choose that the repository be private (which means no one can see your code). 
    - Check the box next to "**Initialize this repository with a README**"
    - Click on the button that says "**Add .gitignore:**" and in the filter type `jekyll`. When **Jekyll** appears as an option, click on it. You can ignore the button that says "Add a license" for now.
    - Go ahead and click on the green button labeled "**Create repository**." This will take you to your new repository page.

{:.py-4 .mt-4 #clone}
***

## 3. Clone Your New Repository

1. On your new repository page, click on the green button in the top right corner labeled "Clone or download."
2. In the box that pops up, click on the button labeled "Open in Desktop." 
    - This action will automatically open GitHub Desktop for you. 
    - GitHub Desktop will ask you to confirm the path of the repository you are cloning to your computer. In most cases, the path that it suggests is fine to use so you can just click on the blue "Clone" button.
3. Now, in the top bar of GitHub Desktop you should see three buttons. On the left, the "Current repository" button lists the repository  you just cloned. In the middle, you can check your current branch (it will probably say master), and on the right there is a button that allows you to "**Fetch origin**," "**Pull origin**," or "**Push origin**." As you work, this button allows you to sync the local version of your repository with the version on GitHub, and push and pull changes between them.

{:.py-4 .mt-4 #add}
***

## 4. Add CollectionBuilder Files

1. In the bar at the top of your GitHub Desktop window, click on "Repository," then click on "Open in Explorer" (if you're on a PC) or "Open in Finder" (if you're on a Mac). 
    - This will show you the location of the repository you just cloned to your computer.
2. Open another Explorer/Finder window, and locate the `Source code (zip)` folder that you downloaded earlier. 
    - Unzip this file and copy and paste the contents into the new repository you have open in the other window.
3. Navigate back to GitHub Desktop. You should see the files you just copied to the repository in the "Changes" column on the left side of the screen.

{:.py-4 .mt-4 #commit}
***

## 5. Committing and Pushing Your New Files

1. Below this list of changes, you'll see a text-entry box labeled "Summary (required)." 
    - This is where you will type your "commit" message, a short message describing the changes you've made. In this case, you might enter something like "upload collectionbuilder repository." 
    - When you've finished your commit message, click on the blue button toward the bottom of the column that says "Commit to master."
2. Now you've committed your changes but haven't pushed them to the online repository yet. To push your commit, click on the button at the top right of the GitHub desktop screen that says "Push changes."
3. **Congratulations, you've pushed your first commit to GitHub!** 
    - If you navigate to your repository on the GitHub web interface now, you'll see that it's been updated with the new files you've added.

{:.py-4 .mt-4 #generate}
***

## 6. Generating Your Site

1. Open GitHub Desktop. In the top bar, click on "Repository," then click on "Open in text editor." (Alternately, this might say "Open in Visual Studio Code" or "Open in Atom.") 
    - This opens your repository in your chosen development environment, a single space that lets you navigate the files in the repository, edit those files in a text editor, and serve or build the project using a terminal window.
2. If the terminal section of VSCode is not open, use the keyboard shortcut `ctrl` + ` (control + backtick) (on both PC and Mac) to open it. 
3. In the terminal, type `jekyll s` and press enter. This "jekyll serve" command will generate the site for you on a local server on your computer. 
4. In the terminal you'll see some text appear, including a URL that appears after the title "Server address:"
5. Hold down `ctrl` and click this link on a PC or hold down `cmd` and click this link on a Mac to open the site in your browser.
6. The generated site will be the demo version of CollectionBuilder. We'll show you soon how to add your own content.
7. When you're ready to end your jekyll session, simply type `ctrl` + `c` (on both PC and Mac) into the terminal. This stops the server from running.

{:.py-4 .mt-4 #edit}
***

## 7. Editing Your Repository

Once you start **customizing your repository**, here are a few things you should know:

1. GitHub Destkop and your text editor (probably VSCode or Atom) are connected, so once you save the changes you make to files in your text editor, those changes will show up in the left-hand "Changes" column in GitHub Desktop. 
    - When you're ready to commit the changes you've made, simply navigate to GitHub Desktop and select the checkboxes next to the files you'd like to commit. 
    - Enter your commit message in the box at the bottom of the column, click the blue "Commit to master" button, and push your changes using the button in the top right of the GitHub Desktop window.
2. If you're working on multiple computers or collaborating, be sure to fetch and pull changes before you push new ones. 
    - You can do this by clicking on the button in the top right of the GitHub Desktop interface labeled "**Fetch origin**." 
    - If there is content to pull, once it is fetched this button will say "**Pull origin**." Click on the button to pull the changes, and you will see your local repository change accordingly.