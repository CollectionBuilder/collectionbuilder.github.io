---
title: Comitting and Pushing Your New Files
stub: commit
section: repository
section_order: 3
---

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
