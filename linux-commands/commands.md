HP@DESKTOP-58G6OEJ MINGW64 /d/Ashiya/JOSH/INTERNSHIP/GIT Advanced/linux-commands (ashiya)
$ git checkout -b git-practice
Switched to a new branch 'git-practice'

HP@DESKTOP-58G6OEJ MINGW64 /d/Ashiya/JOSH/INTERNSHIP/GIT Advanced/linux-commands (git-practice)
$ echo "Initial commit" > file1.txt

HP@DESKTOP-58G6OEJ MINGW64 /d/Ashiya/JOSH/INTERNSHIP/GIT Advanced/linux-commands (git-practice)
$ git add file1.txt
warning: in the working copy of 'linux-commands/file1.txt', LF will be replaced by CRLF the next time Git touches it

HP@DESKTOP-58G6OEJ MINGW64 /d/Ashiya/JOSH/INTERNSHIP/GIT Advanced/linux-commands (git-practice)
$ git commit -m "Initial commit"
[git-practice 8ddb922] Initial commit
 1 file changed, 1 insertion(+)
 create mode 100644 linux-commands/file1.txt

HP@DESKTOP-58G6OEJ MINGW64 /d/Ashiya/JOSH/INTERNSHIP/GIT Advanced/linux-commands (git-practice)
$ echo "Change 1" >> file1.txt

HP@DESKTOP-58G6OEJ MINGW64 /d/Ashiya/JOSH/INTERNSHIP/GIT Advanced/linux-commands (git-practice)
$ git add file1.txt
warning: in the working copy of 'linux-commands/file1.txt', LF will be replaced by CRLF the next time Git touches it

HP@DESKTOP-58G6OEJ MINGW64 /d/Ashiya/JOSH/INTERNSHIP/GIT Advanced/linux-commands (git-practice)
$ git commit -m "Change 1 added"
[git-practice c251dc9] Change 1 added
 1 file changed, 1 insertion(+)

HP@DESKTOP-58G6OEJ MINGW64 /d/Ashiya/JOSH/INTERNSHIP/GIT Advanced/linux-commands (git-practice)
$ git reset --soft HEAD~1

HP@DESKTOP-58G6OEJ MINGW64 /d/Ashiya/JOSH/INTERNSHIP/GIT Advanced/linux-commands (git-practice)
$ git reset --hard HEAD~1
HEAD is now at 3f6a56c Delete oldFile.txt

HP@DESKTOP-58G6OEJ MINGW64 /d/Ashiya/JOSH/INTERNSHIP/GIT Advanced/linux-commands (git-practice)
$ echo "Temporary change" > file1.txt

HP@DESKTOP-58G6OEJ MINGW64 /d/Ashiya/JOSH/INTERNSHIP/GIT Advanced/linux-commands (git-practice)
$ git restore file1.txt
error: pathspec 'file1.txt' did not match any file(s) known to git

HP@DESKTOP-58G6OEJ MINGW64 /d/Ashiya/JOSH/INTERNSHIP/GIT Advanced/linux-commands (git-practice)
$ ls
file1.txt

HP@DESKTOP-58G6OEJ MINGW64 /d/Ashiya/JOSH/INTERNSHIP/GIT Advanced/linux-commands (git-practice)
$ git status -s
?? ./
?? ../new2.txt

HP@DESKTOP-58G6OEJ MINGW64 /d/Ashiya/JOSH/INTERNSHIP/GIT Advanced/linux-commands (git-practice)
$ git ls-files

HP@DESKTOP-58G6OEJ MINGW64 /d/Ashiya/JOSH/INTERNSHIP/GIT Advanced/linux-commands (git-practice)
$ git add file1.txt
warning: in the working copy of 'linux-commands/file1.txt', LF will be replaced by CRLF the next time Git touches it

HP@DESKTOP-58G6OEJ MINGW64 /d/Ashiya/JOSH/INTERNSHIP/GIT Advanced/linux-commands (git-practice)
$ git commit -m "file1.txt"
[git-practice c383a06] file1.txt
 1 file changed, 1 insertion(+)
 create mode 100644 linux-commands/file1.txt

HP@DESKTOP-58G6OEJ MINGW64 /d/Ashiya/JOSH/INTERNSHIP/GIT Advanced/linux-commands (git-practice)
$ echo "Temporarily changed file1" > file1.txt

HP@DESKTOP-58G6OEJ MINGW64 /d/Ashiya/JOSH/INTERNSHIP/GIT Advanced/linux-commands (git-practice)
$ git restore file1.txt

HP@DESKTOP-58G6OEJ MINGW64 /d/Ashiya/JOSH/INTERNSHIP/GIT Advanced/linux-commands (git-practice)
$ git switch ashiya
Switched to branch 'ashiya'

HP@DESKTOP-58G6OEJ MINGW64 /d/Ashiya/JOSH/INTERNSHIP/GIT Advanced/linux-commands (ashiya)
$ git switch git-practice
Switched to branch 'git-practice'

HP@DESKTOP-58G6OEJ MINGW64 /d/Ashiya/JOSH/INTERNSHIP/GIT Advanced/linux-commands (git-practice)
$ git remote -v
origin-github   git@github.com:AshiyaAjare/GIT-Advanced-Assignment.git (fetch)
origin-github   git@github.com:AshiyaAjare/GIT-Advanced-Assignment.git (push)
origin-gitlab   https://gitlab.com/AshiyaAjare/git_advanced.git (fetch)
origin-gitlab   https://gitlab.com/AshiyaAjare/git_advanced.git (push)

HP@DESKTOP-58G6OEJ MINGW64 /d/Ashiya/JOSH/INTERNSHIP/GIT Advanced/linux-commands (git-practice)
$ git fecth -a
git: 'fecth' is not a git command. See 'git --help'.

The most similar command is
        fetch

HP@DESKTOP-58G6OEJ MINGW64 /d/Ashiya/JOSH/INTERNSHIP/GIT Advanced/linux-commands (git-practice)
$ git fetch -a

HP@DESKTOP-58G6OEJ MINGW64 /d/Ashiya/JOSH/INTERNSHIP/GIT Advanced/linux-commands (git-practice)
$ git reflog
c383a06 (HEAD -> git-practice) HEAD@{0}: checkout: moving from ashiya to git-practice
3f6a56c (origin-github/ashiya, ashiya) HEAD@{1}: checkout: moving from git-practice to ashiya
c383a06 (HEAD -> git-practice) HEAD@{2}: commit: file1.txt
3f6a56c (origin-github/ashiya, ashiya) HEAD@{3}: reset: moving to HEAD~1
8ddb922 HEAD@{4}: reset: moving to HEAD~1
c251dc9 HEAD@{5}: commit: Change 1 added
8ddb922 HEAD@{6}: commit: Initial commit
3f6a56c (origin-github/ashiya, ashiya) HEAD@{7}: checkout: moving from ashiya to git-practice
3f6a56c (origin-github/ashiya, ashiya) HEAD@{8}: merge origin-github/ashiya: Fast-forward
11b85a8 (master) HEAD@{9}: checkout: moving from master to ashiya
11b85a8 (master) HEAD@{10}: commit: update the repository
9608dd7 (origin-gitlab/master) HEAD@{11}: commit: Initial commit
d5018f5 (fix, feature2) HEAD@{12}: checkout: moving from feature2 to master
d5018f5 (fix, feature2) HEAD@{13}: commit: change the file name
7f8005f HEAD@{14}: commit: changes made to feature2 branch
8c5f79c HEAD@{15}: checkout: moving from feature2 to feature2
8c5f79c HEAD@{16}: checkout: moving from feature1 to feature2
a688764 (feature1) HEAD@{17}: commit: Change file1 in feature1
78d7fa6 HEAD@{18}: checkout: moving from feature2 to feature1

HP@DESKTOP-58G6OEJ MINGW64 /d/Ashiya/JOSH/INTERNSHIP/GIT Advanced/linux-commands (git-practice)
$ git checkout -b feature-branch
Switched to a new branch 'feature-branch'

HP@DESKTOP-58G6OEJ MINGW64 /d/Ashiya/JOSH/INTERNSHIP/GIT Advanced/linux-commands (feature-branch)
$ echo "Feature-content" > feature.txt

HP@DESKTOP-58G6OEJ MINGW64 /d/Ashiya/JOSH/INTERNSHIP/GIT Advanced/linux-commands (feature-branch)
$ git add feature.txt
warning: in the working copy of 'linux-commands/feature.txt', LF will be replaced by CRLF the next time Git touches it

HP@DESKTOP-58G6OEJ MINGW64 /d/Ashiya/JOSH/INTERNSHIP/GIT Advanced/linux-commands (feature-branch)
$ git commit =m "Feature added"
error: pathspec '=m' did not match any file(s) known to git
error: pathspec 'Feature added' did not match any file(s) known to git

HP@DESKTOP-58G6OEJ MINGW64 /d/Ashiya/JOSH/INTERNSHIP/GIT Advanced/linux-commands (feature-branch)
$ git commit -m "Feature added"
[feature-branch 293def3] Feature added
 1 file changed, 1 insertion(+)
 create mode 100644 linux-commands/feature.txt

HP@DESKTOP-58G6OEJ MINGW64 /d/Ashiya/JOSH/INTERNSHIP/GIT Advanced/linux-commands (feature-branch)
$ git swiitch git-practice
git: 'swiitch' is not a git command. See 'git --help'.

The most similar command is
        switch

HP@DESKTOP-58G6OEJ MINGW64 /d/Ashiya/JOSH/INTERNSHIP/GIT Advanced/linux-commands (feature-branch)
$ git switch git-practice
Switched to branch 'git-practice'

HP@DESKTOP-58G6OEJ MINGW64 /d/Ashiya/JOSH/INTERNSHIP/GIT Advanced/linux-commands (git-practice)
$ git rebase "feature-branch"
Successfully rebased and updated refs/heads/git-practice.

HP@DESKTOP-58G6OEJ MINGW64 /d/Ashiya/JOSH/INTERNSHIP/GIT Advanced/linux-commands (git-practice)
$ echo "Added content" >> file1.txt

HP@DESKTOP-58G6OEJ MINGW64 /d/Ashiya/JOSH/INTERNSHIP/GIT Advanced/linux-commands (git-practice)
$ git add file1.txt
warning: in the working copy of 'linux-commands/file1.txt', LF will be replaced by CRLF the next time Git touches it

HP@DESKTOP-58G6OEJ MINGW64 /d/Ashiya/JOSH/INTERNSHIP/GIT Advanced/linux-commands (git-practice)
$ git commit --amend -m "Update commit with new content"
[git-practice 11bc3cf] Update commit with new content
 Date: Mon Jan 6 18:17:50 2025 +0530
 2 files changed, 2 insertions(+)
 create mode 100644 linux-commands/feature.txt

HP@DESKTOP-58G6OEJ MINGW64 /d/Ashiya/JOSH/INTERNSHIP/GIT Advanced/linux-commands (git-practice)
$ git log
commit 11bc3cfb3264c3d616b4e3d02373202e74ebff27 (HEAD -> git-practice)
Author: Ashiya <ashiyaajare6@gmail.com>
Date:   Mon Jan 6 18:17:50 2025 +0530

    Update commit with new content

commit c383a0624d021acdbb1530b342717335cc53afdc
Author: Ashiya <ashiyaajare6@gmail.com>
Date:   Mon Jan 6 18:12:22 2025 +0530

    file1.txt

commit 3f6a56c9cbf4aa99c87b85843b543742241de12d (origin-github/ashiya, ashiya)
Author: AshiyaAjare <ashiya.ajare@joshsoftware.com>
Date:   Sun Jan 5 18:38:43 2025 +0530

    Delete oldFile.txt

commit efcdf6ed5fc54d960226b55e9f6de5ea1621dd2d
Author: AshiyaAjare <ashiya.ajare@joshsoftware.com>
Date:   Sun Jan 5 18:38:26 2025 +0530

    Delete newFile.txt


HP@DESKTOP-58G6OEJ MINGW64 /d/Ashiya/JOSH/INTERNSHIP/GIT Advanced/linux-commands (git-practice)
$

HP@DESKTOP-58G6OEJ MINGW64 /d/Ashiya/JOSH/INTERNSHIP/GIT Advanced/linux-commands (git-practice)
$ git cherr-pick c383a0624d021acdbb1530b342717335cc53afdc
git: 'cherr-pick' is not a git command. See 'git --help'.

The most similar command is
        cherry-pick

HP@DESKTOP-58G6OEJ MINGW64 /d/Ashiya/JOSH/INTERNSHIP/GIT Advanced/linux-commands (git-practice)
$ git cherry-pick c383a0624d021acdbb1530b342717335cc53afdc
Auto-merging linux-commands/file1.txt
CONFLICT (add/add): Merge conflict in linux-commands/file1.txt
error: could not apply c383a06... file1.txt
hint: After resolving the conflicts, mark them with
hint: "git add/rm <pathspec>", then run
hint: "git cherry-pick --continue".
hint: You can instead skip this commit with "git cherry-pick --skip".
hint: To abort and get back to the state before "git cherry-pick",
hint: run "git cherry-pick --abort".

HP@DESKTOP-58G6OEJ MINGW64 /d/Ashiya/JOSH/INTERNSHIP/GIT Advanced/linux-commands (git-practice|CHERRY-PICKING)
$ git cherry-pick 11bc3cfb3264c3d616b4e3d02373202e74ebff27
error: Cherry-picking is not possible because you have unmerged files.
hint: Fix them up in the work tree, and then use 'git add/rm <file>'
hint: as appropriate to mark resolution and make a commit.
fatal: cherry-pick failed

HP@DESKTOP-58G6OEJ MINGW64 /d/Ashiya/JOSH/INTERNSHIP/GIT Advanced/linux-commands (git-practice|CHERRY-PICKING)
$ git add linux-commands/file1.txt
warning: could not open directory 'linux-commands/linux-commands/': No such file or directory
fatal: pathspec 'linux-commands/file1.txt' did not match any files

HP@DESKTOP-58G6OEJ MINGW64 /d/Ashiya/JOSH/INTERNSHIP/GIT Advanced/linux-commands (git-practice|CHERRY-PICKING)
$ git add file1.txt

HP@DESKTOP-58G6OEJ MINGW64 /d/Ashiya/JOSH/INTERNSHIP/GIT Advanced/linux-commands (git-practice|CHERRY-PICKING)
$ git cherry-pick --continue
hint: Waiting for your editor to close the file... unix2dos: converting file D:/Ashiya/JOSH/INTERNSHIP/GIT Advanced/.git/COMMIT_EDITMSG to DOS format...
dos2unix: converting file D:/Ashiya/JOSH/INTERNSHIP/GIT Advanced/.git/COMMIT_EDITMSG to Unix format...
[git-practice 13391a6] cherry pick file1.txt
 Date: Mon Jan 6 18:12:22 2025 +0530
 1 file changed, 3 insertions(+)

HP@DESKTOP-58G6OEJ MINGW64 /d/Ashiya/JOSH/INTERNSHIP/GIT Advanced/linux-commands (git-practice)
$ git status
On branch git-practice
Untracked files:
  (use "git add <file>..." to include in what will be committed)
        ../new2.txt

nothing added to commit but untracked files present (use "git add" to track)

HP@DESKTOP-58G6OEJ MINGW64 /d/Ashiya/JOSH/INTERNSHIP/GIT Advanced/linux-commands (git-practice)
$ echo "temporary sample file" >> file1.txt

HP@DESKTOP-58G6OEJ MINGW64 /d/Ashiya/JOSH/INTERNSHIP/GIT Advanced/linux-commands (git-practice)
$ git stash
warning: in the working copy of 'linux-commands/file1.txt', LF will be replaced by CRLF the next time Git touches it
Saved working directory and index state WIP on git-practice: 13391a6 cherry pick file1.txt

HP@DESKTOP-58G6OEJ MINGW64 /d/Ashiya/JOSH/INTERNSHIP/GIT Advanced/linux-commands (git-practice)
$ git stash pop
On branch git-practice
Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   file1.txt

Untracked files:
  (use "git add <file>..." to include in what will be committed)
        ../new2.txt

no changes added to commit (use "git add" and/or "git commit -a")
Dropped refs/stash@{0} (55d960a99ae1be8cde61566973ce20edcd37cf2e)

HP@DESKTOP-58G6OEJ MINGW64 /d/Ashiya/JOSH/INTERNSHIP/GIT Advanced/linux-commands (git-practice)
$ git checkout -b merge-branch
Switched to a new branch 'merge-branch'

HP@DESKTOP-58G6OEJ MINGW64 /d/Ashiya/JOSH/INTERNSHIP/GIT Advanced/linux-commands (merge-branch)
$ echo "file to be merged" > merge.txt

HP@DESKTOP-58G6OEJ MINGW64 /d/Ashiya/JOSH/INTERNSHIP/GIT Advanced/linux-commands (merge-branch)
$ git add merge.txt
warning: in the working copy of 'linux-commands/merge.txt', LF will be replaced by CRLF the next time Git touches it

HP@DESKTOP-58G6OEJ MINGW64 /d/Ashiya/JOSH/INTERNSHIP/GIT Advanced/linux-commands (merge-branch)
$ git commit -m "Add merge file"
[merge-branch 4a97f06] Add merge file
 1 file changed, 1 insertion(+)
 create mode 100644 linux-commands/merge.txt

HP@DESKTOP-58G6OEJ MINGW64 /d/Ashiya/JOSH/INTERNSHIP/GIT Advanced/linux-commands (merge-branch)
$ git checkout git-practice
Switched to branch 'git-practice'
M       linux-commands/file1.txt

HP@DESKTOP-58G6OEJ MINGW64 /d/Ashiya/JOSH/INTERNSHIP/GIT Advanced/linux-commands (git-practice)
$ git merge merge-branch
Updating 13391a6..4a97f06
Fast-forward
 linux-commands/merge.txt | 1 +
 1 file changed, 1 insertion(+)
 create mode 100644 linux-commands/merge.txt

HP@DESKTOP-58G6OEJ MINGW64 /d/Ashiya/JOSH/INTERNSHIP/GIT Advanced/linux-commands (git-practice)
$ git merge --squash merge-branch
Already up to date. (nothing to squash)

HP@DESKTOP-58G6OEJ MINGW64 /d/Ashiya/JOSH/INTERNSHIP/GIT Advanced/linux-commands (git-practice)
$ git push origin-github git-practice
Enumerating objects: 18, done.
Counting objects: 100% (18/18), done.
Delta compression using up to 4 threads
Compressing objects: 100% (12/12), done.
Writing objects: 100% (17/17), 1.41 KiB | 206.00 KiB/s, done.
Total 17 (delta 1), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (1/1), done.
remote:
remote: Create a pull request for 'git-practice' on GitHub by visiting:
remote:      https://github.com/AshiyaAjare/GIT-Advanced-Assignment/pull/new/git-practice
remote:
To github.com:AshiyaAjare/GIT-Advanced-Assignment.git
 * [new branch]      git-practice -> git-practice

HP@DESKTOP-58G6OEJ MINGW64 /d/Ashiya/JOSH/INTERNSHIP/GIT Advanced/linux-commands (git-practice)
$
