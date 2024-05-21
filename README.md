## Git advanced 
# Exercise 1 part 2 part 6
```bash
 git checkout -b ft/new-branch-from-commit  320a956d153d65b9fe35d8c62568ac01eb48d874
Switched to a new branch 'ft/new-branch-from-commit'
PS C:\Users\alexa\Desktop\git-advanced> git add .    
PS C:\Users\alexa\Desktop\git-advanced> git commit -m "Create menu" 
[ft/new-branch-from-commit 9e1bf4e] Create menu
 1 file changed, 19 insertions(+)
 create mode 100644 index.html
PS C:\Users\alexa\Desktop\git-advanced> git checkout main
Switched to branch 'main'
Your branch is up to date with 'origin/main'.
PS C:\Users\alexa\Desktop\git-advanced> git pull origin main
From https://github.com/AL2002MI08/git-advanced-exercises
 * branch            main       -> FETCH_HEAD
Already up to date.
PS C:\Users\alexa\Desktop\git-advanced> git branch
  ft/branch
  ft/new-branch-from-commit
* main
PS C:\Users\alexa\Desktop\git-advanced> git merge ft/new-branch-from-commit
Merge made by the 'ort' strategy.
 index.html | 19 +++++++++++++++++++
 1 file changed, 19 insertions(+)
 create mode 100644 index.html
PS C:\Users\alexa\Desktop\git-advanced> git checkout ft/new-branch-from-commit
Switched to branch 'ft/new-branch-from-commit'
PS C:\Users\alexa\Desktop\git-advanced> git status
On branch ft/new-branch-from-commit
nothing to commit, working tree clean
PS C:\Users\alexa\Desktop\git-advanced> git push
fatal: The current branch ft/new-branch-from-commit has no upstream branch.
To push the current branch and set the remote as upstream, use

    git push --set-upstream origin ft/new-branch-from-commit

To have this happen automatically for branches without a tracking
upstream, see 'push.autoSetupRemote' in 'git help config'.

PS C:\Users\alexa\Desktop\git-advanced>  git push --set-upstream origin ft/new-branch-from-commit   
Enumerating objects: 4, done.
Counting objects: 100% (4/4), done.
Delta compression using up to 12 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 477 bytes | 238.00 KiB/s, done.
Total 3 (delta 1), reused 0 (delta 0), pack-reused 0 (from 0)
remote: Resolving deltas: 100% (1/1), completed with 1 local object.
remote:
remote: Create a pull request for 'ft/new-branch-from-commit' on GitHub by visiting:
remote:      https://github.com/AL2002MI08/git-advanced-exercises/pull/new/ft/new-branch-from-commit
pick 320a956 Implemented core functionality for new feature
remote:
To https://github.com/AL2002MI08/git-advanced-exercises.git
 * [new branch]      ft/new-branch-from-commit -> ft/new-branch-from-commit
branch 'ft/new-branch-from-commit' set up to track 'origin/ft/new-branch-from-commit'.
PS C:\Users\alexa\Desktop\git-advanced> git checkout main
Switched to branch 'main'
Your branch is ahead of 'origin/main' by 2 commits.
  (use "git push" to publish your local commits)
PS C:\Users\alexa\Desktop\git-advanced> git pull origin main
From https://github.com/AL2002MI08/git-advanced-exercises
 * branch            main       -> FETCH_HEAD
Already up to date.
PS C:\Users\alexa\Desktop\git-advanced> git merge ft/new-branch-from-commit
Already up to date.
PS C:\Users\alexa\Desktop\git-advanced> git rebase -i HEAD~2
Successfully rebased and updated refs/heads/main.
PS C:\Users\alexa\Desktop\git-advanced> git log
commit 2844e549c061c8567609b34bf687ad172b953072 (HEAD -> main)
Author: AL2002MI08 <alexandramizero@gmail.com>
Date:   Tue May 21 06:26:22 2024 +0200

    Create menu

commit 05c4e40c56b83409798603ade0f377019373aace
Author: AL2002MI08 <alexandramizero@gmail.com>
Date:   Tue May 21 05:41:19 2024 +0200

    Implemented core functionality for new feature

commit 0301b44ecfbe5edd9ab129a3c27793e5d0581cd0
Author: AL2002MI08 <alexandramizero@gmail.com>
Date:   Tue May 21 05:45:25 2024 +0200
PS C:\Users\alexa\Desktop\git-advanced> git reflog
2844e54 (HEAD -> main) HEAD@{0}: rebase (finish): returning to refs/heads/main
2844e54 (HEAD -> main) HEAD@{1}: rebase (pick): Create menu
05c4e40 HEAD@{2}: rebase (pick): Implemented core functionality for new feature
0301b44 HEAD@{3}: rebase (start): checkout HEAD~2
ccea1ea HEAD@{4}: checkout: moving from ft/new-branch-from-commit to main
9e1bf4e (origin/ft/new-branch-from-commit, ft/new-branch-from-commit) HEAD@{5}: checkout: moving from main to ft/new-branch-from-commit
ccea1ea HEAD@{6}: merge ft/new-branch-from-commit: Merge made by the 'ort' strategy.
c5108f0 (origin/main) HEAD@{7}: checkout: moving from ft/new-branch-from-commit to main
9e1bf4e (origin/ft/new-branch-from-commit, ft/new-branch-from-commit) HEAD@{8}: commit: Create menu
320a956 HEAD@{9}: checkout: moving from main to ft/new-branch-from-commit
c5108f0 (origin/main) HEAD@{10}: merge ft/new-feature: Merge made by the 'ort' strategy.
0301b44 HEAD@{11}: commit: Updated project readme
68cde5f HEAD@{12}: checkout: moving from ft/new-feature to main
320a956 HEAD@{13}: commit: Implemented core functionality for new feature
68cde5f HEAD@{14}: checkout: moving from main to ft/new-feature
PS C:\Users\alexa\Desktop\git-advanced> 
 *  History restored 

PS C:\Users\alexa\Desktop\git-advanced> git branch
  ft/branch
  ft/new-branch-from-commit
* main
PS C:\Users\alexa\Desktop\git-advanced> git checkout ft/new-branch-from-commit
Switched to branch 'ft/new-branch-from-commit'
Your branch is up to date with 'origin/ft/new-branch-from-commit'.
PS C:\Users\alexa\Desktop\git-advanced> git rebase main
warning: skipped previously applied commit 320a956
warning: skipped previously applied commit 9e1bf4e
hint: use --reapply-cherry-picks to include skipped commits
hint: Disable this message with "git config advice.skippedCherryPicks false"
Successfully rebased and updated refs/heads/ft/new-branch-from-commit.
PS C:\Users\alexa\Desktop\git-advanced> git log --grep="cherry picked from commit"
PS C:\Users\alexa\Desktop\git-advanced> git log
commit 2844e549c061c8567609b34bf687ad172b953072 (HEAD -> ft/new-branch-from-commit, main)
Author: AL2002MI08 <alexandramizero@gmail.com>
Date:   Tue May 21 06:26:22 2024 +0200

    Create menu

commit 05c4e40c56b83409798603ade0f377019373aace
Author: AL2002MI08 <alexandramizero@gmail.com>
Date:   Tue May 21 05:41:19 2024 +0200

    Implemented core functionality for new feature

commit 0301b44ecfbe5edd9ab129a3c27793e5d0581cd0
Author: AL2002MI08 <alexandramizero@gmail.com>
Date:   Tue May 21 05:45:25 2024 +0200

    Updated project readme

commit 68cde5f18631945f12e6ed5ddaf091745e094931
Author: AL2002MI08 <alexandramizero@gmail.com>
Date:   Mon May 20 19:38:40 2024 +0200

    Implemented test7

commit 357e81cb3cf87bd6e84399f4565eadc549db56c7
Author: AL2002MI08 <alexandramizero@gmail.com>
Date:   Mon May 20 18:20:34 2024 +0200

    chore: Create fifth file

commit 3babf85fe9485c02b524ae4e23220e920ea03933
Author: AL2002MI08 <alexandramizero@gmail.com>
Date:   Mon May 20 17:28:32 2024 +0200

    chore: Create fourth file

commit 20029380de1d759642fae8bd484180ac59b56f52
Author: AL2002MI08 <alexandramizero@gmail.com>
Date:   Mon May 20 18:21:14 2024 +0200

    chore: Create sixth file

commit 9efd3a28a0d257075d44243c8afdb75235c95287
Author: AL2002MI08 <alexandramizero@gmail.com>
Date:   Mon May 20 17:26:40 2024 +0200

    chore: Create third file

commit 4dd186af13a645bc960292f88c51632cba00556f
Author: AL2002MI08 <alexandramizero@gmail.com>
Date:   Mon May 20 17:17:19 2024 +0200

    chore: Combine first/second file

commit 2b44d7283b4a715b5bc1d61e3e3e5df64c69968e
Author: AL2002MI08 <alexandramizero@gmail.com>
Date:   Mon May 20 16:45:39 2024 +0200

    added Readme file
PS C:\Users\alexa\Desktop\git-advanced> git checkout main
Merge ft/feature-branch-from commit to 'main' of https://github.com/AL2002MI08/git-advanced-exercises
Switched to branch 'main'
Your branch and 'origin/main' have diverged,
and have 2 and 2 different commits each, respectively.
  (use "git pull" if you want to integrate the remote branch with yours)
PS C:\Users\alexa\Desktop\git-advanced> git branch
  ft/branch
  ft/new-branch-from-commit
* main
PS C:\Users\alexa\Desktop\git-advanced> git merge ft/new-branch-from-commit
Already up to date.
PS C:\Users\alexa\Desktop\git-advanced> git pull
Merge made by the 'ort' strategy.
PS C:\Users\alexa\Desktop\git-advanced> git branch -m  ft/new-branch-from-commit ft/improved-branch-menu
PS C:\Users\alexa\Desktop\git-advanced> git branch
  ft/branch
  ft/improved-branch-menu
* main
PS C:\Users\alexa\Desktop\git-advanced> git log
commit 2f4df6b4728e9599e54d5f1240fb6e4331f2c4d4 (HEAD -> main)
Merge: 2844e54 c5108f0
Author: AL2002MI08 <alexandramizero@gmail.com>
Date:   Tue May 21 08:35:42 2024 +0200

    Merge ft/feature-branch-from commit to 'main' of https://github.com/AL2002MI08/git-advanced-exercises

commit 2844e549c061c8567609b34bf687ad172b953072 (ft/improved-branch-menu)
Author: AL2002MI08 <alexandramizero@gmail.com>
Date:   Tue May 21 06:26:22 2024 +0200

    Create menu

commit 05c4e40c56b83409798603ade0f377019373aace
Author: AL2002MI08 <alexandramizero@gmail.com>
PS C:\Users\alexa\Desktop\git-advanced> git checkout 2f4df6b4728e9599e54d5f1240fb6e4331f2c4d4
Note: switching to '2f4df6b4728e9599e54d5f1240fb6e4331f2c4d4'.

You are in 'detached HEAD' state. You can look around, make experimental
changes and commit them, and you can discard any commits you make in this
state without impacting any branches by switching back to a branch.

If you want to create a new branch to retain commits you create, you may
do so (now or later) by using -c with the switch command. Example:

  git switch -c <new-branch-name>

Or undo this operation with:

  git switch -

Turn off this advice by setting config variable advice.detachedHead to false

HEAD is now at 2f4df6b Merge ft/feature-branch-from commit to 'main' of https://github.com/AL2002MI08/git-advanced-exercises
PS C:\Users\alexa\Desktop\git-advanced> git log
commit 2f4df6b4728e9599e54d5f1240fb6e4331f2c4d4 (HEAD, main)
Merge: 2844e54 c5108f0
Author: AL2002MI08 <alexandramizero@gmail.com>
Date:   Tue May 21 08:35:42 2024 +0200

    Merge ft/feature-branch-from commit to 'main' of https://github.com/AL2002MI08/git-advanced-exercises

commit 2844e549c061c8567609b34bf687ad172b953072 (ft/improved-branch-menu)
Author: AL2002MI08 <alexandramizero@gmail.com>
Date:   Tue May 21 06:26:22 2024 +0200

    Create menu

commit 05c4e40c56b83409798603ade0f377019373aace
Author: AL2002MI08 <alexandramizero@gmail.com>
:...skipping...
commit 2f4df6b4728e9599e54d5f1240fb6e4331f2c4d4 (HEAD, main)
Merge: 2844e54 c5108f0
Author: AL2002MI08 <alexandramizero@gmail.com>
Date:   Tue May 21 08:35:42 2024 +0200

    Merge ft/feature-branch-from commit to 'main' of https://github.com/AL2002MI08/git-advanced-exercises

commit 2844e549c061c8567609b34bf687ad172b953072 (ft/improved-branch-menu)
Author: AL2002MI08 <alexandramizero@gmail.com>
Date:   Tue May 21 06:26:22 2024 +0200

    Create menu

commit 05c4e40c56b83409798603ade0f377019373aace
Author: AL2002MI08 <alexandramizero@gmail.com>
Date:   Tue May 21 05:41:19 2024 +0200

    Implemented core functionality for new feature

commit c5108f0a60d6b7b47d6840c675f4697046692e08 (origin/main)
Merge: 0301b44 320a956
Author: AL2002MI08 <alexandramizero@gmail.com>
Date:   Tue May 21 06:02:44 2024 +0200

    Merge branch 'ft/new-feature' with main

commit 0301b44ecfbe5edd9ab129a3c27793e5d0581cd0
Author: AL2002MI08 <alexandramizero@gmail.com>
PS C:\Users\alexa\Desktop\git-advanced> git checkout main
M       README.md
Switched to branch 'main'
Your branch is ahead of 'origin/main' by 3 commits.
  (use "git push" to publish your local commits)
PS C:\Users\alexa\Desktop\git-advanced> git branch
  ft/branch
  ft/improved-branch-menu
* main
PS C:\Users\alexa\Desktop\git-advanced> git status
On branch main
Your branch is ahead of 'origin/main' by 3 commits.
  (use "git push" to publish your local commits)

Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   README.md

no changes added to commit (use "git add" and/or "git commit -a")
PS C:\Users\alexa\Desktop\git-advanced> git add . 
PS C:\Users\alexa\Desktop\git-advanced> git commit -m "modified Readme file"
[main cfe080d] modified Readme file
 1 file changed, 286 insertions(+), 1 deletion(-)
PS C:\Users\alexa\Desktop\git-advanced> git push
Enumerating objects: 12, done.
Counting objects: 100% (11/11), done.
Delta compression using up to 12 threads
Compressing objects: 100% (8/8), done.
Writing objects: 100% (8/8), 3.62 KiB | 1.81 MiB/s, done.
Total 8 (delta 3), reused 0 (delta 0), pack-reused 0 (from 0)
remote: Resolving deltas: 100% (3/3), completed with 1 local object.
To https://github.com/AL2002MI08/git-advanced-exercises.git
   c5108f0..cfe080d  main -> main
```