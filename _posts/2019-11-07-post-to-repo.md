---
layout: post
title: "Add Project to Git"
date: 2019-11-07
---

1. Create a new repository on GitHub. To avoid errors, do not initialize the new repository with README, license, or gitignore files. You can add these files after your project has been pushed to GitHub.
2. Open Terminal.
3. Change the current working directory to your local project.
4. Initialize the local directory as a Git repository.
    <code>$ git init</code>

5. Add the files in your new local repository. This stages them for the first commit.
    <br><code>$ git add .</code>
    # Adds the files in the local repository and stages them for commit. To unstage a file, use 'git reset HEAD YOUR-FILE'.

6. Commit the files that you've staged in your local repository.
    <code>$ git commit -m "First commit"</code>
    # Commits the tracked changes and prepares them to be pushed to a remote repository. To remove this commit and modify the file, use 'git reset --soft HEAD~1' and commit and add the file again.

7. At the top of your GitHub repository's Quick Setup page, click  to copy the remote repository URL.
8. In Terminal, add the URL for the remote repository where your local repository will be pushed.
    <code>$ git remote add origin remote repository URL# Sets the new remote</code>
    <code>$ git remote -v</code>
    # Verifies the new remote URL
9. Push the changes in your local repository to GitHub.
    <code>$ git push origin master</code>
    # Pushes the changes in your local repository up to the remote repository you specified as the origin
