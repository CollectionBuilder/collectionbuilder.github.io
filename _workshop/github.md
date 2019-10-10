---
title: Git and GitHub Setup
step: 2
---

## 1. Get an Account
Create an account on [GitHub](https://github.com){:target="_blank"}. When you sign up, GitHub will send you an email with instructions that you need to follow in order to verify your account, so be sure to complete this step before you begin working.

{:.py-4 .mt-4 #}
***

## 2. Connect Your Account
Connect your GitHub account information to Git on your computer. To do this, open up a terminal window and enter these commands (the user name and user email should match those you use for you GitHub account):

```
git config --global user.name "Evan Will"
git config --global user.email "myemail@gmail.com"
```

> Your email and user name is recorded with every commit.
> This helps ensure integrity and authenticity of the history.
> Most people keep their email public, but if you are concerned about privacy, check GitHub's tips to [hide your email](https://help.github.com/articles/about-commit-email-addresses/){:target="_blank"}.

{:.py-4 .mt-4 #}
***

## 3. Download the Latest CollectionBuilder Release

1. Log in to the [GitHub](https://github.com){:target="_blank"} web interface and go to our [cb-skin](){:target="_blank"} repository.
2. The main page of a repository is the "Code" tab, which has a representation of the files, and displays the `README`. Navigate to the latest project release. You can do this by clicking on the "Releases" tab, which you'll find in the second navigation bar, below the row the "Code" tab is in. 
3. Download the `Source code (zip)` folder.

{:.py-4 .mt-4 #}
***

## 4. Create a New Repository

1. Navigate back to your own GitHub account Repositories page.
2. In the top right corner, click on the green button labeled "New."
3. This brings you to a "Create a new repository" form. Follow these steps:
    - Enter your new repository name, and give your project a description. 
    - If you have a free account you will have to make the respository public, but if you have a paid account or are part of an organization, you can choose that the repository be private (which means no one can see your code). 
    - Check the box next to "Initialize this repository with a README"
    - Click on the button that says "Add .gitignore:" and in the filter type "jekyll." When "Jekyll" appears as an option, click on it. You can ignore the button that says "Add a license" for now.
    - Go ahead and click on the green button labeled "Create repository." This will take you to your new repository page.

{:.py-4 .mt-4 #}
***

## 4. Clone Your New Repository

1. On your new repository page, click on the green button in the top right corner labeled "Clone or download."
2. In the box that pops up, click on the button labeled "Open in Desktop." 
    - This action will automatically open GitHub Desktop for you. 
    - GitHub Desktop will ask you to confirm the path of the repository you are cloning to your computer. In most cases, the path that it suggests is fine to use so you can just click on the blue "Clone" button.
3. Now, in the top bar of GitHub Desktop you should see three buttons. On the left, the "Current repository" button lists the repository  you just cloned. In the middle, you can check your current branch (it will probably say master), and on the right there is a button that allows you to "Fetch origin," "Pull changes," or "Push changes." As you work, this button allows you to sync the local version of your repository with the version on GitHub, and push and pull changes between them.

{:.py-4 .mt-4 #}
***

## 5. Add CollectionBuilder Files

1. In the bar at the top of your GitHub Desktop window, click on "Repository," then click on "Open in Explorer" (if you're on a PC) or "Open in Finder" (if you're on a Mac). This will show you the location of the repository you just cloned to your computer.
2. Open another Explorer/Finder window, and locate the `Source code (zip)` folder that you downloaded earlier. Unzip this file and copy and paste the contents into the new repository you have open in the other window.
3. Navigate back to GitHub Desktop. You should see the files you just copied to the repository in the "Changes" column to the left side of the screen.

{:.py-4 .mt-4 #}
***

## 6. Committing and Pushing Your New Files

1. Below this list of changes, you'll see a text-entry box labeled "Summary (required)." This is where you will type your "commit" message, a short message describing the changes you've made. In this case, you might enter something like "upload collectionbuilder repository." When you've finished your commit message, click on the blue button toward the bottom of the column that says "Commit to master."
2. Now you've committed your changes but haven't pushed them to the online repository yet. To push your commit, click on the button at the top right of the GitHub desktop screen that says "Push changes."
3. Congratulations, you've pushed your first commit to GitHub! If you navigate to your repository on the GitHub web interface now, you'll see that it's been updated with the new files you've added.

{:.py-4 .mt-4 #}
***

## 7. Editing Your Repository

1. Now it's time to start customizing your repository. Open your GitHub Desktop window again. 
2. In the top bar, click on "Repository," then click on "Open in text editor." (Alternately, this might say "Open in Visual Studio Code" or "Open in Atom.") This opens your repository in your chosen development environment, a single space that lets you navigate the files in the repository, edit those files in a text editor, and serve or build the project using a terminal window.
3. GitHub Destkop and your text editor (probably VSCode or Atom) are connected, so once you save the changes you make to files in your text editor, those changes will show up in the left-hand "Changes" column in GitHub Desktop. When you're ready to commit the changes you've made, simply navigate to GitHub Desktop and select the checkboxes next to the files you'd like to commit. Enter your commit message in the box at the bottom of the column, click the blue "Commit to master" button, and push your changes using the button in the top right of the GitHub Desktop window.
4. If you're working on multiple computers or collaborating, be sure to fetch and pull changes before you push new ones. You can do this by clicking on the button in the top right of the GitHub Desktop interface labeled "Fetch origin." If there is content to pull, once it is fetched this button will say "Pull changes." Click on the button to pull the changes, and you will see your local repository change accordingly.

{:.py-4 .mt-4 #}
***

### You're all set up to begin working on your collection! Proceed to the Metadata page to learn the next steps.

