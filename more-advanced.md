# Answers
>by Joanne

**What is the difference between git reset and git revert. When would you use one over the other?**
*git revert  creates a new commit that undoes the changes from a previous commit. This command adds new history to the project (it doesn't modify existing history).*
*checks-out content from the repository and puts it in your work tree. It can also have other effects, depending on how the command was invoked. For instance, it can also change which branch you are currently working on. This command doesn't make any changes to the history.*
*If a commit has been made somewhere in the project's history, and you later decide that the commit is wrong and should not have been done, then git revert is the tool for the job. It will undo the changes introduced by the bad commit, recording the "undo" in the history.*
*If you have made a commit, but haven't shared it with anyone else and you decide you don't want it, then you can use git reset to rewrite the history so that it looks as though you never made that commit.*

**What is the difference between git merge and git rebase. When would you use one over the other?**
*Git rebase and merge both integrate changes from one branch into another. Where they differ is how it's done. Git rebase moves a feature branch into a master. Git merge adds a new commit, preserving the history.*
*If you're working alone or on a small team, use rebase. If you're working with a big team, use merge.*

**What is the difference between git stash pop and git stash apply. When would you use one over the other?**
*git stash pop throws away the (topmost, by default) stash after applying it, whereas git stash apply leaves it in the stash list for possible later reuse (or you can then git stash drop it).*
*This happens unless there are conflicts after git stash pop, in which case it will not remove the stash, leaving it to behave exactly like git stash apply.*
*Another way to look at it: git stash pop is git stash apply && git stash drop.*

**What kinds of things can you do in interactive mode when rebasing?**
*Interactive rebasing can be used for changing commits in many ways such as editing, deleting, and squashing. To tell Git where to start the interactive rebase, use the SHA-1 or index of the commit that immediately precedes the commit you want to modify.*