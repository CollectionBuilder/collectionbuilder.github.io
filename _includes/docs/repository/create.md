
{:.py-4 .mt-4 #create}
***

## 1. Create a New Repository

First, set up a repository on GitHub for your CollectionBuilder project.
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