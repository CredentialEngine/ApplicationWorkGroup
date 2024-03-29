# Steps to Contribute

1. Browse to https://github.com/CredentialEngine/ApplicationWorkGroup
2. Click the fork button
3. Clone the repository to your machine using: `git clone https://github.com/CredentialEngine/ApplicationWorkGroup`, replacing `username` with your Github username.
4. Change to the 'ApplicationWorkGroup' directory
5. Verify that git is configured properly. Specifically, make sure that your name and email in your local machine settings match the name and email associated with your Github profile.
    ```
    git config user.email
    git config user.name
    ```
    
    If the values do not match your Github profile, you can set them with the following, replacing `email@example.com` and `Example User` with the values that match your Github profile. NOTE: This will only change the configuration for the `
    ` repository. If you want to change it for all repositories, use `git config --global` instead.
    ```
    git config user.email "email@example.com"
    git config user.name "Example User"
    ```
    
6. Create a branch for you work using `git checkout -b branch-name`, replacing `branch-name` with a name to reflect the work that you are doing. For example, if you are working on issue #45, you might name your branch `issue_45`.
7. Make your modifications using your favorite text editor.
8. Verify your changes are what you want. You can use `git diff` to see all the changes that you have made.
9. If the changes are what you want, then commit the source code using the following.

    **IT IS IMPORTANT TO INCLUDE THE `-s` OPTION TO SIGN YOUR COMMIT.**
    ```
    git add .
    git commit -s -m "insert message reflecting what you changed"
    ```
 
10. **Optional:**  If you performed multiple commits on your local branch, you can squash these commits using `git rebase -i HEAD~<# of commits>`. For example, to squash four commits into one, do the following:
    ```
    git rebase -i HEAD~4
    ```

    In the text editor that comes up, keep the word `pick` for the first commit and replace the words `pick` with `squash` next to all other commits. Save and close the editor, and git will combine the "squash"'ed commits with the one before it. Git will then give you the opportunity to change your commit message to something like, "Issue #100: Fixed retweet bug." Make sure that your commit message also contains the DCO sign-off line.

    **Important**: If you've already pushed commits to GitHub, and then squash them locally, you will have to force the push to your branch.
    ```
    git push origin branch-name --force
    ```

    Helpful hint: Before doing a push, you can always edit your last commit message, before pushing, by using:
    ```
    git commit --amend -s
    ```
    
    The `-s` option will add the necessary line for the DCO sign-off.

11. Push your changes, replacing `branch-name` with the branch name that you created above.
    ```
    git push origin branch-name
    ```
    
12. Create a new pull request by visiting `https://github.com/username/ApplicationWorkGroup`, replacing `username` with your Github username. Click the "New Pull Request" button.

13. Verify that the pull request contains your commits and that all commits are signed off prior to creating the pull request.

# References
* [Installing Git](https://git-scm.com/book/en/v2/Getting-Started-Installing-Git)
* [Git Workflow](https://tkuhrt.github.io/git-workflow/)
* [Video: Configuring Github and Submitting Your Pull Request](https://www.youtube.com/watch?v=f5XZe7dv0_U)
* [Setting Your Username in Git](https://help.github.com/articles/setting-your-username-in-git/)
* [Setting Your Email in Git](https://help.github.com/articles/setting-your-commit-email-address-in-git/)
