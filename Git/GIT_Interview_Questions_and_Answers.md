## GIT Interview Questions

1. **What is Git?**
    - Git is a distributed version control system that tracks changes in source code during software development. It allows multiple collaborators to work on a project, manage versions, and merge their changes seamlessly.


2. **What are the benefits of using Git?**
    - Benefits include version control, collaboration, code history, branching and merging, reliability, and support for both small and large projects.


3. **What is a repository in Git?**
    - A repository (or repo) in Git is a directory where all the project's files, history, and configuration are stored. It contains the complete version history of the project.


4. **How does Git differ from other version control systems?**
    - Git is distributed, meaning every developer has a local copy of the repository. It's faster, more flexible, and supports branching and merging effectively.


5. **What are the different stages in Git?**
    - The three main stages in Git are:
        1. Working Directory (untracked and modified files).
        2. Staging Area (files prepared for commit).
        3. Repository (committed files with version history).


6. **How do you create a new branch in Git?**
    - Use the command: `git checkout -b branch_name`.


7. **How do you switch between branches in Git?**
    - Use the command: `git checkout branch_name`.


8. **What is a merge conflict in Git, and how do you resolve it?**
    - A merge conflict occurs when two branches have conflicting changes. To resolve it, edit the conflicting files, mark them as resolved, and commit the changes.


9. **What is the difference between a fast-forward merge and a three-way merge?**
    - A fast-forward merge applies changes from a source branch to a target branch directly, while a three-way merge combines changes from two divergent branches using a common ancestor.

| Aspect             | Fast-Forward Merge                      | Three-Way Merge                        |
|--------------------|----------------------------------------|----------------------------------------|
| **Merge Type**     | Merges a branch's changes directly into the current branch if they have a linear history and no conflicting changes. | Merges changes from two divergent branches, combining their modifications and resolving conflicts if they exist. |
| **Commit History** | Results in a linear commit history, with the current branch advancing directly. | Preserves the commit history of both branches, showing where they diverged and where they were merged. |
| **Conflicts**      | Typically no merge conflicts, as it assumes a linear history with no conflicting changes. | May involve merge conflicts if changes in both branches overlap or conflict with each other. |
| **Use Cases**      | Appropriate for feature branches or hotfixes when there is no need to maintain the full history of the source branch. | Suitable for merging complex or divergent branches with extensive commit histories and potential conflicts. |
| **Command Example** | `git merge source_branch`                | `git merge source_branch`                |


10. **What is the purpose of the "git clone" command?**
    - `git clone` is used to create a copy of a remote repository on your local machine for development or collaboration.


11. **How do you undo the last commit in Git?**
    - Use `git reset HEAD~1` to undo the last commit and preserve changes in your working directory.


12. **How do you discard local changes in Git?**
    - Use `git checkout -- file_name` to discard changes in a specific file, or `git reset --hard` to discard all local changes.


13. **What is the purpose of the "git rebase" command?**
    - `git rebase` is used to apply the changes from one branch on top of another, creating a linear commit history.


14. **How do you create a tag in Git?**
    - Use `git tag -a tag_name -m "Tag message"` to create an annotated tag, or `git tag tag_name` for a lightweight tag.


15. **What is a remote in Git?**
    - A remote is a named reference to a remote repository, allowing you to interact with repositories on other servers.


16. **How do you push changes to a remote repository in Git?**
    - Use `git push remote_name branch_name` to push changes to a remote repository.


17. **How do you pull changes from a remote repository in Git?**
    - Use `git pull remote_name branch_name` to fetch and merge changes from a remote repository.


18. **What is the difference between "git fetch" and "git pull"?**
    - `git fetch` downloads changes from a remote repository but does not merge them, while `git pull` downloads and merges changes in one step.

| Aspect             | `git fetch`                             | `git pull`                              |
|--------------------|----------------------------------------|----------------------------------------|
| **Purpose**        | Downloads changes from a remote repository to your local repository but doesn't automatically merge them. | Downloads changes from a remote repository and immediately merges them into the current branch. |
| **Commit Changes** | Fetching changes doesn't affect your working branch; it only updates the remote branch references. | Pulling changes not only updates remote branch references but also incorporates them into your working branch. |
| **Use Cases**      | Useful when you want to see what changes are available on the remote branch before merging or to update your local references. | Suitable for quickly incorporating remote changes into your local branch without manually merging. |
| **Command Example** | `git fetch origin`                      | `git pull origin branch_name`           |


19. **How do you resolve a merge conflict during a pull request on GitHub?**
    - In GitHub, merge conflicts are resolved by editing the conflicting files directly on the platform or locally, pushing the changes, and confirming the merge.


20. **What is Git rebase workflow, and when is it used?**
    - The Git rebase workflow involves moving or combining a sequence of commits to a new base commit. It's used to maintain a linear and cleaner commit history, particularly when working on feature branches.