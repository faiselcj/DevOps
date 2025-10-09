🧩 1. Git Configuration & Setup
Used when setting up Git for the first time or changing settings.
git config --global user.name "Your Name"
git config --global user.email "your@email.com"
git config --list                # Show all configurations
git config --global core.editor "code --wait"
________________________________________
📁 2. Repository Initialization
To start or clone a repository.
git init                        # Initialize a new local repo
git clone <repo_url>            # Clone an existing repo
________________________________________
📄 3. Basic Snapshotting
To track changes in files.
git status                      # Show changed files
git add <file>                  # Stage a single file
git add .                       # Stage all changes
git reset <file>                # Unstage a file
git diff                        # Show unstaged changes
git diff --staged               # Show staged changes
________________________________________
💾 4. Committing Changes
To record the changes in your repository.
git commit -m "Commit message"         # Commit staged changes
git commit -am "Commit message"        # Add + commit tracked files
git log                                # Show commit history
git show <commit_id>                   # Show details of a specific commit
________________________________________
🔁 5. Branching & Merging
Branching is key in DevOps workflows (feature branches, CI/CD pipelines, etc.)
git branch                             # List branches
git branch <name>                      # Create a new branch
git checkout <branch>                  # Switch branch
git checkout -b <branch>               # Create + switch branch
git merge <branch>                     # Merge a branch into current
git branch -d <branch>                 # Delete a branch
git branch -D <branch>                 # Force delete a branch
________________________________________
🔄 6. Synchronizing with Remote
DevOps teams work in distributed repos — so syncing is crucial.
git remote -v                         # Show remote URLs
git remote add origin <url>           # Link to remote repo
git fetch                             # Get latest changes from remote
git pull                              # Fetch + merge remote changes
git push                              # Push local commits to remote
git push -u origin <branch>           # Push branch and set upstream
________________________________________
🧰 7. Undoing Changes
To fix mistakes safely.
git checkout -- <file>                # Discard local changes
git restore <file>                    # (newer) Restore file to last commit
git reset --soft HEAD~1               # Undo last commit (keep changes staged)
git reset --hard HEAD~1               # Undo last commit (discard changes)
git revert <commit_id>                # Create a new commit that undoes previous commit
________________________________________
🎯 8. Tagging (for Releases)
Tags are used in DevOps for marking release versions.
git tag v1.0                          # Create a lightweight tag
git tag -a v1.0 -m "Release 1.0"      # Annotated tag
git push origin v1.0                  # Push tag to remote
git push origin --tags                # Push all tags
________________________________________
⚙️ 9. Stashing
To save temporary work without committing.
git stash                             # Save uncommitted changes
git stash list                        # List stashes
git stash pop                         # Reapply last stash
git stash drop                        # Delete last stash
________________________________________
🔍 10. Inspection & Comparison
For troubleshooting and auditing in DevOps pipelines.
git log --oneline --graph --decorate  # Compact commit tree
git show <commit_id>                  # Show a commit details
git diff <branch1>..<branch2>         # Compare branches
git blame <file>                      # Show who changed each line
________________________________________
🧮 11. Cherry-Picking
To apply a specific commit from another branch.
git cherry-pick <commit_id>
________________________________________
🚀 12. Advanced Remote Commands
Often used in CI/CD scripts.
git fetch --all                       # Fetch all branches
git pull origin main                  # Pull latest main branch
git push origin --delete <branch>     # Delete remote branch
git remote prune origin               # Clean up deleted branches
________________________________________
🧑‍💻 13. Rebase (for Clean History)
Rebasing makes history linear before merges or deployments.
git rebase <branch>                   # Rebase onto another branch
git rebase --continue                 # Continue after conflicts
git rebase --abort                    # Cancel rebase
________________________________________
🧱 14. Submodules (for Microservices/Dependencies)
Useful when managing multiple repos in DevOps.
git submodule add <repo_url>
git submodule update --init --recursive
________________________________________
🧼 15. Clean-up & Maintenance
Keep repos healthy and optimized.
git gc                                # Clean up unnecessary files
git clean -f                          # Remove untracked files
________________________________________
🧭 16. DevOps CI/CD Git Tips
In CI/CD pipelines (like Jenkins, Azure DevOps, GitHub Actions), you often see:
git fetch origin
git checkout $BRANCH_NAME
git pull origin $BRANCH_NAME
git tag $RELEASE_VERSION
git push origin --tags

