# Konecta
Konecta Git tasks

Explain what git stash does and when it is useful.
git stash is a very handy Git command that temporarily shelves (or "stashes") changes you've made to your working directory so you can work on something else without committing the changes. It's like hitting "pause" on your current work to quickly address an urgent task, and then picking up right where you left off.
Interruptions: If you're in the middle of working on a feature and need to switch to another branch to fix a critical bug.
Context Switching: When you need to jump between different tasks or features without cluttering your commit history with incomplete work.
Cleaning Up: If you want to quickly clean up your working directory without losing your changes.
Experimenting: To test some changes without committing them.

Use git stash to temporarily save uncommitted changes.
To temporarily save uncommitted changes using git stash, you can run: git stash

List and describe the stashed changes.
List Stashes: Use the following command to display a list of all the stashes you have saved: git stash list
Show a Stash: To see a summary of the changes in a specific stash, use: git stash show stash@{N}
Show Detailed Diff: If you want a detailed view of the changes in a specific stash, use: git stash show -p stash@{N}

Restore stashed changes using the appropriate command.
To reapply the most recent stash to your working directory, use: git stash apply
To apply a specific stash from the list, use: git stash apply stash@{N}
To reapply the most recent stash and remove it from your stash list, use: git stash pop
To pop a specific stash from the list, use: 
git stash pop stash@{N}

Apply and remove a specific stash.
List Your Stashes: git stash list
Apply a Specific Stash: git stash apply stash@{N}
Remove a Specific Stash: git stash drop stash@{N}
Combine Both with git stash pop
Pop a Specific Stash: git stash pop stash@{N}

Drop or clear all stashes from the stash list.
Run the following command to remove all stashes from your stash list: git stash clear

What happens when you use git stash pop vs git stash apply?
The git stash apply command re-applies the changes from a stash to your working directory without removing the stash from the stash list.
The git stash pop command re-applies the changes from a stash to your working directory and then removes the stash from the stash list.

What is the purpose of git stash save "message"?
The git stash save "message" command allows you to stash your changes with a custom message. This can help you keep track of different stashes by providing context for each one.

How can you stash changes for specific files instead of the entire working directory?
Stashing changes for specific files can be done using the git stash push command with the -m flag.
git stash push -m "Stashing changes for specific files" path/to/file1 path/to/file2

How can you check which files were affected in a particular stash?
You can check which files were affected in a particular stash by using the git stash show command
git stash show stash@{N}
git stash show -p stash@{N}
