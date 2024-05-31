# 1 git_tutorial

```bash


xiluo@DESKTOP-AFIBLVR MINGW64 /f/WorkSpace/Github
$ mkdir git_tutorial

xiluo@DESKTOP-AFIBLVR MINGW64 /f/WorkSpace/Github
$ ls
'Git 资料.lnk'*   git_tutorial/

xiluo@DESKTOP-AFIBLVR MINGW64 /f/WorkSpace/Github
$ cd git_tutorial/

xiluo@DESKTOP-AFIBLVR MINGW64 /f/WorkSpace/Github/git_tutorial
$ ls

xiluo@DESKTOP-AFIBLVR MINGW64 /f/WorkSpace/Github/git_tutorial
$ git init
Initialized empty Git repository in F:/WorkSpace/Github/git_tutorial/.git/

xiluo@DESKTOP-AFIBLVR MINGW64 /f/WorkSpace/Github/git_tutorial (master)
$ git status
On branch master

No commits yet

nothing to commit (create/copy files and use "git add" to track)

xiluo@DESKTOP-AFIBLVR MINGW64 /f/WorkSpace/Github/git_tutorial (master)
$ touch README.md

xiluo@DESKTOP-AFIBLVR MINGW64 /f/WorkSpace/Github/git_tutorial (master)
$ git status
On branch master

No commits yet

Untracked files:
  (use "git add <file>..." to include in what will be committed)
        README.md

nothing added to commit but untracked files present (use "git add" to track)

xiluo@DESKTOP-AFIBLVR MINGW64 /f/WorkSpace/Github/git_tutorial (master)
$ git add README.md

xiluo@DESKTOP-AFIBLVR MINGW64 /f/WorkSpace/Github/git_tutorial (master)
$ git status
On branch master

No commits yet

Changes to be committed:
  (use "git rm --cached <file>..." to unstage)
        new file:   README.md


xiluo@DESKTOP-AFIBLVR MINGW64 /f/WorkSpace/Github/git_tutorial (master)
$ git commit -m "First commit"
[master (root-commit) 9f14bde] First commit
 1 file changed, 0 insertions(+), 0 deletions(-)
 create mode 100644 README.md

xiluo@DESKTOP-AFIBLVR MINGW64 /f/WorkSpace/Github/git_tutorial (master)
$ git status
On branch master
nothing to commit, working tree clean

xiluo@DESKTOP-AFIBLVR MINGW64 /f/WorkSpace/Github/git_tutorial (master)
$ git log
commit 9f14bde42aae54c95919890c0567bdc6f40989ea (HEAD -> master)
Author: Shiel <2910747383@qq.com>
Date:   Tue May 21 15:24:11 2024 +0800

    First commit

xiluo@DESKTOP-AFIBLVR MINGW64 /f/WorkSpace/Github/git_tutorial (master)
$ git remote -v

xiluo@DESKTOP-AFIBLVR MINGW64 /f/WorkSpace/Github/git_tutorial (master)
$ git log README.md
commit 9f14bde42aae54c95919890c0567bdc6f40989ea (HEAD -> master)
Author: Shiel <2910747383@qq.com>
Date:   Tue May 21 15:24:11 2024 +0800

    First commit

xiluo@DESKTOP-AFIBLVR MINGW64 /f/WorkSpace/Github/git_tutorial (master)
$ git log -p
commit 9f14bde42aae54c95919890c0567bdc6f40989ea (HEAD -> master)
Author: Shiel <2910747383@qq.com>
Date:   Tue May 21 15:24:11 2024 +0800

    First commit

diff --git a/README.md b/README.md
new file mode 100644
index 0000000..e69de29

xiluo@DESKTOP-AFIBLVR MINGW64 /f/WorkSpace/Github/git_tutorial (master)
$ git log -p README.md
commit 9f14bde42aae54c95919890c0567bdc6f40989ea (HEAD -> master)
Author: Shiel <2910747383@qq.com>
Date:   Tue May 21 15:24:11 2024 +0800

    First commit

diff --git a/README.md b/README.md
new file mode 100644
index 0000000..e69de29

xiluo@DESKTOP-AFIBLVR MINGW64 /f/WorkSpace/Github/git_tutorial (master)
$ vim README.md

xiluo@DESKTOP-AFIBLVR MINGW64 /f/WorkSpace/Github/git_tutorial (master)
$ git diff
diff --git a/README.md b/README.md
index e69de29..ec80c56 100644
--- a/README.md
+++ b/README.md
@@ -0,0 +1 @@
+# Git 教程

xiluo@DESKTOP-AFIBLVR MINGW64 /f/WorkSpace/Github/git_tutorial (master)
$ git add README.md

xiluo@DESKTOP-AFIBLVR MINGW64 /f/WorkSpace/Github/git_tutorial (master)
$ git diff

xiluo@DESKTOP-AFIBLVR MINGW64 /f/WorkSpace/Github/git_tutorial (master)
$ git diff head
diff --git a/README.md b/README.md
index e69de29..ec80c56 100644
--- a/README.md
+++ b/README.md
@@ -0,0 +1 @@
+# Git 教程

xiluo@DESKTOP-AFIBLVR MINGW64 /f/WorkSpace/Github/git_tutorial (master)
$ git commit -m "Add index"
[master d414820] Add index
 1 file changed, 1 insertion(+)

xiluo@DESKTOP-AFIBLVR MINGW64 /f/WorkSpace/Github/git_tutorial (master)
$ git log
commit d41482024113f28391edc2e53576847f43feee87 (HEAD -> master)
Author: Shiel <2910747383@qq.com>
Date:   Tue May 21 15:28:04 2024 +0800

    Add index

commit 9f14bde42aae54c95919890c0567bdc6f40989ea
Author: Shiel <2910747383@qq.com>
Date:   Tue May 21 15:24:11 2024 +0800

    First commit

xiluo@DESKTOP-AFIBLVR MINGW64 /f/WorkSpace/Github/git_tutorial (master)
$ git branch
* master

xiluo@DESKTOP-AFIBLVR MINGW64 /f/WorkSpace/Github/git_tutorial (master)
$ git checkout -b feature_A
Switched to a new branch 'feature_A'

xiluo@DESKTOP-AFIBLVR MINGW64 /f/WorkSpace/Github/git_tutorial (feature_A)
$ git branch
* feature_A
  master

xiluo@DESKTOP-AFIBLVR MINGW64 /f/WorkSpace/Github/git_tutorial (feature_A)
$ vim README.md

xiluo@DESKTOP-AFIBLVR MINGW64 /f/WorkSpace/Github/git_tutorial (feature_A)
$

xiluo@DESKTOP-AFIBLVR MINGW64 /f/WorkSpace/Github/git_tutorial (feature_A)
$ git add README.md

xiluo@DESKTOP-AFIBLVR MINGW64 /f/WorkSpace/Github/git_tutorial (feature_A)
$ git commit -m "Add feature_A"
[feature_A 125ae4f] Add feature_A
 1 file changed, 2 insertions(+)

xiluo@DESKTOP-AFIBLVR MINGW64 /f/WorkSpace/Github/git_tutorial (feature_A)
$ git checkout master
Switched to branch 'master'

xiluo@DESKTOP-AFIBLVR MINGW64 /f/WorkSpace/Github/git_tutorial (master)
$ vim
.git/      README.md

xiluo@DESKTOP-AFIBLVR MINGW64 /f/WorkSpace/Github/git_tutorial (master)
$ vim
.git/      README.md

xiluo@DESKTOP-AFIBLVR MINGW64 /f/WorkSpace/Github/git_tutorial (master)
$ vim README.md

xiluo@DESKTOP-AFIBLVR MINGW64 /f/WorkSpace/Github/git_tutorial (master)
$ git checkout -
Switched to branch 'feature_A'

xiluo@DESKTOP-AFIBLVR MINGW64 /f/WorkSpace/Github/git_tutorial (feature_A)
$ git branch
* feature_A
  master

xiluo@DESKTOP-AFIBLVR MINGW64 /f/WorkSpace/Github/git_tutorial (feature_A)
$ git checkout -
Switched to branch 'master'

xiluo@DESKTOP-AFIBLVR MINGW64 /f/WorkSpace/Github/git_tutorial (master)
$ git merge --no-ff feature_A
Merge made by the 'ort' strategy.
 README.md | 2 ++
 1 file changed, 2 insertions(+)

xiluo@DESKTOP-AFIBLVR MINGW64 /f/WorkSpace/Github/git_tutorial (master)
$ git log --graph
*   commit b90a352d988a418eb2a0ace9372b526291f36a4b (HEAD -> master)
|\  Merge: d414820 125ae4f
| | Author: Shiel <2910747383@qq.com>
| | Date:   Tue May 21 15:33:04 2024 +0800
| |
| |     Merge branch 'feature_A'
| |
| * commit 125ae4f308db4709b575a5010d21a0ea7a4f762b (feature_A)
|/  Author: Shiel <2910747383@qq.com>
|   Date:   Tue May 21 15:30:40 2024 +0800
|
|       Add feature_A
|
* commit d41482024113f28391edc2e53576847f43feee87
| Author: Shiel <2910747383@qq.com>
| Date:   Tue May 21 15:28:04 2024 +0800
|
|     Add index
|
* commit 9f14bde42aae54c95919890c0567bdc6f40989ea
  Author: Shiel <2910747383@qq.com>
  Date:   Tue May 21 15:24:11 2024 +0800

      First commit

xiluo@DESKTOP-AFIBLVR MINGW64 /f/WorkSpace/Github/git_tutorial (master)
$ git reset --hard d41482024113f28391edc2e53576847f43feee87
HEAD is now at d414820 Add index

xiluo@DESKTOP-AFIBLVR MINGW64 /f/WorkSpace/Github/git_tutorial (master)
$ git checkout -b fix_B
Switched to a new branch 'fix_B'

xiluo@DESKTOP-AFIBLVR MINGW64 /f/WorkSpace/Github/git_tutorial (fix_B)
$ ls
README.md

xiluo@DESKTOP-AFIBLVR MINGW64 /f/WorkSpace/Github/git_tutorial (fix_B)
$ vim
.git/      README.md

xiluo@DESKTOP-AFIBLVR MINGW64 /f/WorkSpace/Github/git_tutorial (fix_B)
$ vim README.md

xiluo@DESKTOP-AFIBLVR MINGW64 /f/WorkSpace/Github/git_tutorial (fix_B)
$ git add README.md

xiluo@DESKTOP-AFIBLVR MINGW64 /f/WorkSpace/Github/git_tutorial (fix_B)
$ git commit -m "Fix B"
[fix_B 0b4a36e] Fix B
 1 file changed, 2 insertions(+)

xiluo@DESKTOP-AFIBLVR MINGW64 /f/WorkSpace/Github/git_tutorial (fix_B)
$ git log --graph
* commit 0b4a36e1391dd06fd95bd4487105e28b85ea44da (HEAD -> fix_B)
| Author: Shiel <2910747383@qq.com>
| Date:   Tue May 21 15:37:11 2024 +0800
|
|     Fix B
|
* commit d41482024113f28391edc2e53576847f43feee87 (master)
| Author: Shiel <2910747383@qq.com>
| Date:   Tue May 21 15:28:04 2024 +0800
|
|     Add index
|
* commit 9f14bde42aae54c95919890c0567bdc6f40989ea
  Author: Shiel <2910747383@qq.com>
  Date:   Tue May 21 15:24:11 2024 +0800

      First commit

xiluo@DESKTOP-AFIBLVR MINGW64 /f/WorkSpace/Github/git_tutorial (fix_B)
$ git reflog
0b4a36e (HEAD -> fix_B) HEAD@{0}: commit: Fix B
d414820 (master) HEAD@{1}: checkout: moving from master to fix_B
d414820 (master) HEAD@{2}: reset: moving to d41482024113f28391edc2e53576847f43fee
b90a352 HEAD@{3}: merge feature_A: Merge made by the 'ort' strategy.
d414820 (master) HEAD@{4}: checkout: moving from feature_A to master
125ae4f (feature_A) HEAD@{5}: checkout: moving from master to feature_A
d414820 (master) HEAD@{6}: checkout: moving from feature_A to master
125ae4f (feature_A) HEAD@{7}: commit: Add feature_A
d414820 (master) HEAD@{8}: checkout: moving from master to feature_A
d414820 (master) HEAD@{9}: commit: Add index
9f14bde HEAD@{10}: commit (initial): First commit

xiluo@DESKTOP-AFIBLVR MINGW64 /f/WorkSpace/Github/git_tutorial (fix_B)
$ git checkout master
Switched to branch 'master'

xiluo@DESKTOP-AFIBLVR MINGW64 /f/WorkSpace/Github/git_tutorial (master)
$ git reset --hard b90a352
HEAD is now at b90a352 Merge branch 'feature_A'

xiluo@DESKTOP-AFIBLVR MINGW64 /f/WorkSpace/Github/git_tutorial (master)
$ git log --graph
*   commit b90a352d988a418eb2a0ace9372b526291f36a4b (HEAD -> master)
|\  Merge: d414820 125ae4f
| | Author: Shiel <2910747383@qq.com>
| | Date:   Tue May 21 15:33:04 2024 +0800
| |
| |     Merge branch 'feature_A'
| |
| * commit 125ae4f308db4709b575a5010d21a0ea7a4f762b (feature_A)
|/  Author: Shiel <2910747383@qq.com>
|   Date:   Tue May 21 15:30:40 2024 +0800
|
|       Add feature_A
|
* commit d41482024113f28391edc2e53576847f43feee87
| Author: Shiel <2910747383@qq.com>
| Date:   Tue May 21 15:28:04 2024 +0800
|
|     Add index
|
* commit 9f14bde42aae54c95919890c0567bdc6f40989ea
  Author: Shiel <2910747383@qq.com>
  Date:   Tue May 21 15:24:11 2024 +0800

      First commit

xiluo@DESKTOP-AFIBLVR MINGW64 /f/WorkSpace/Github/git_tutorial (master)
$ git merge --no-ff fix_B
Auto-merging README.md
CONFLICT (content): Merge conflict in README.md
Automatic merge failed; fix conflicts and then commit the result.

xiluo@DESKTOP-AFIBLVR MINGW64 /f/WorkSpace/Github/git_tutorial (master|MERGING)
$ vim README.md

xiluo@DESKTOP-AFIBLVR MINGW64 /f/WorkSpace/Github/git_tutorial (master|MERGING)
$ git add README.md

xiluo@DESKTOP-AFIBLVR MINGW64 /f/WorkSpace/Github/git_tutorial (master|MERGING)
$ git commit -m "Fix conflict"
[master 366687f] Fix conflict

xiluo@DESKTOP-AFIBLVR MINGW64 /f/WorkSpace/Github/git_tutorial (master)
$ git commit --amend
[master e57335c] Merge branch 'fix_B'
 Date: Tue May 21 16:03:34 2024 +0800

xiluo@DESKTOP-AFIBLVR MINGW64 /f/WorkSpace/Github/git_tutorial (master)
$ git lof --graph
git: 'lof' is not a git command. See 'git --help'.

The most similar command is
        log

xiluo@DESKTOP-AFIBLVR MINGW64 /f/WorkSpace/Github/git_tutorial (master)
$ git log --graph
*   commit e57335cab86bb76985dbccfe4e4b331f41622e62 (HEAD -> master)
|\  Merge: b90a352 0b4a36e
| | Author: Shiel <2910747383@qq.com>
| | Date:   Tue May 21 16:03:34 2024 +0800
| |
| |     Merge branch 'fix_B'
| |
| * commit 0b4a36e1391dd06fd95bd4487105e28b85ea44da (fix_B)
| | Author: Shiel <2910747383@qq.com>
| | Date:   Tue May 21 15:37:11 2024 +0800
| |
| |     Fix B
| |
* |   commit b90a352d988a418eb2a0ace9372b526291f36a4b
|\ \  Merge: d414820 125ae4f
| |/  Author: Shiel <2910747383@qq.com>
|/|   Date:   Tue May 21 15:33:04 2024 +0800
| |
| |       Merge branch 'feature_A'
| |
| * commit 125ae4f308db4709b575a5010d21a0ea7a4f762b (feature_A)
|/  Author: Shiel <2910747383@qq.com>
|   Date:   Tue May 21 15:30:40 2024 +0800
|
|       Add feature_A
|
* commit d41482024113f28391edc2e53576847f43feee87
| Author: Shiel <2910747383@qq.com>
| Date:   Tue May 21 15:28:04 2024 +0800
|
|     Add index
|
* commit 9f14bde42aae54c95919890c0567bdc6f40989ea
  Author: Shiel <2910747383@qq.com>
  Date:   Tue May 21 15:24:11 2024 +0800

      First commit

xiluo@DESKTOP-AFIBLVR MINGW64 /f/WorkSpace/Github/git_tutorial (master)
$ git checkout -b feature_C
Switched to a new branch 'feature_C'

xiluo@DESKTOP-AFIBLVR MINGW64 /f/WorkSpace/Github/git_tutorial (feature_C)
$ git branch
  feature_A
* feature_C
  fix_B
  master

xiluo@DESKTOP-AFIBLVR MINGW64 /f/WorkSpace/Github/git_tutorial (feature_C)
$ ls
README.md

xiluo@DESKTOP-AFIBLVR MINGW64 /f/WorkSpace/Github/git_tutorial (feature_C)
$ vim README.md

xiluo@DESKTOP-AFIBLVR MINGW64 /f/WorkSpace/Github/git_tutorial (feature_C)
$ git commit -am "Add feature_C"
[feature_C f56c30d] Add feature_C
 1 file changed, 1 insertion(+)

xiluo@DESKTOP-AFIBLVR MINGW64 /f/WorkSpace/Github/git_tutorial (feature_C)
$ vim README.md

xiluo@DESKTOP-AFIBLVR MINGW64 /f/WorkSpace/Github/git_tutorial (feature_C)
$ git diff
diff --git a/README.md b/README.md
index 24a9eab..0794145 100644
--- a/README.md
+++ b/README.md
@@ -2,4 +2,4 @@

     - feature_A
     - fix_B
-    - faeture_C
+    - feature_C

xiluo@DESKTOP-AFIBLVR MINGW64 /f/WorkSpace/Github/git_tutorial (feature_C)
$ git commit -am "Fix typo"
[feature_C 5de05d8] Fix typo
 1 file changed, 1 insertion(+), 1 deletion(-)

xiluo@DESKTOP-AFIBLVR MINGW64 /f/WorkSpace/Github/git_tutorial (feature_C)
$ git rebase -i HEAD~2
Successfully rebased and updated refs/heads/feature_C.

xiluo@DESKTOP-AFIBLVR MINGW64 /f/WorkSpace/Github/git_tutorial (feature_C)
$ git rebase -i HEAD~2
Auto-merging README.md
CONFLICT (content): Merge conflict in README.md
error: could not apply 0b4a36e... Fix B
hint: Resolve all conflicts manually, mark them as resolved with
hint: "git add/rm <conflicted_files>", then run "git rebase --continue".
hint: You can instead skip this commit: run "git rebase --skip".
hint: To abort and get back to the state before "git rebase", run "git rebase --abort".
hint: Disable this message with "git config advice.mergeConflict false"
Could not apply 0b4a36e... Fix B

xiluo@DESKTOP-AFIBLVR MINGW64 /f/WorkSpace/Github/git_tutorial (feature_C|REBASE 1/2)
$ git rebase -i HEAD~2
fatal: It seems that there is already a rebase-merge directory, and
I wonder if you are in the middle of another rebase.  If that is the
case, please try
        git rebase (--continue | --abort | --skip)
If that is not the case, please
        rm -fr ".git/rebase-merge"
and run me again.  I am stopping in case you still have something
valuable there.


xiluo@DESKTOP-AFIBLVR MINGW64 /f/WorkSpace/Github/git_tutorial (feature_C|REBASE 1/2)
$ git rebase -i HEAD~2
fatal: It seems that there is already a rebase-merge directory, and
I wonder if you are in the middle of another rebase.  If that is the
case, please try
        git rebase (--continue | --abort | --skip)
If that is not the case, please
        rm -fr ".git/rebase-merge"
and run me again.  I am stopping in case you still have something
valuable there.


xiluo@DESKTOP-AFIBLVR MINGW64 /f/WorkSpace/Github/git_tutorial (feature_C|REBASE 1/2)
$ git log --graph
*   commit b90a352d988a418eb2a0ace9372b526291f36a4b (HEAD)
|\  Merge: d414820 125ae4f
| | Author: Shiel <2910747383@qq.com>
| | Date:   Tue May 21 15:33:04 2024 +0800
| |
| |     Merge branch 'feature_A'
| |
| * commit 125ae4f308db4709b575a5010d21a0ea7a4f762b (feature_A)
|/  Author: Shiel <2910747383@qq.com>
|   Date:   Tue May 21 15:30:40 2024 +0800
|
|       Add feature_A
|
* commit d41482024113f28391edc2e53576847f43feee87
| Author: Shiel <2910747383@qq.com>
| Date:   Tue May 21 15:28:04 2024 +0800
|
|     Add index
|
* commit 9f14bde42aae54c95919890c0567bdc6f40989ea
  Author: Shiel <2910747383@qq.com>
  Date:   Tue May 21 15:24:11 2024 +0800

      First commit

xiluo@DESKTOP-AFIBLVR MINGW64 /f/WorkSpace/Github/git_tutorial (feature_C|REBASE 1/2)
$ ls
README.md

xiluo@DESKTOP-AFIBLVR MINGW64 /f/WorkSpace/Github/git_tutorial (feature_C|REBASE 1/2)
$ vim README.md

xiluo@DESKTOP-AFIBLVR MINGW64 /f/WorkSpace/Github/git_tutorial (feature_C|REBASE 1/2)
$ git reset --hard e57335cab86bb76985dbccfe4e4b331f41622e62
HEAD is now at e57335c Merge branch 'fix_B'

xiluo@DESKTOP-AFIBLVR MINGW64 /f/WorkSpace/Github/git_tutorial (feature_C|REBASE 1/2)
$ git log
commit e57335cab86bb76985dbccfe4e4b331f41622e62 (HEAD, master)
Merge: b90a352 0b4a36e
Author: Shiel <2910747383@qq.com>
Date:   Tue May 21 16:03:34 2024 +0800

    Merge branch 'fix_B'

commit 0b4a36e1391dd06fd95bd4487105e28b85ea44da (fix_B)
Author: Shiel <2910747383@qq.com>
Date:   Tue May 21 15:37:11 2024 +0800

    Fix B

commit b90a352d988a418eb2a0ace9372b526291f36a4b
Merge: d414820 125ae4f
Author: Shiel <2910747383@qq.com>
Date:   Tue May 21 15:33:04 2024 +0800

    Merge branch 'feature_A'

commit 125ae4f308db4709b575a5010d21a0ea7a4f762b (feature_A)
Author: Shiel <2910747383@qq.com>
Date:   Tue May 21 15:30:40 2024 +0800

    Add feature_A

commit d41482024113f28391edc2e53576847f43feee87
Author: Shiel <2910747383@qq.com>
Date:   Tue May 21 15:28:04 2024 +0800

    Add index

commit 9f14bde42aae54c95919890c0567bdc6f40989ea
Author: Shiel <2910747383@qq.com>
Date:   Tue May 21 15:24:11 2024 +0800


xiluo@DESKTOP-AFIBLVR MINGW64 /f/WorkSpace/Github/git_tutorial (feature_C|REBASE 1/2)
$ git log --graph
*   commit e57335cab86bb76985dbccfe4e4b331f41622e62 (HEAD, master)
|\  Merge: b90a352 0b4a36e
| | Author: Shiel <2910747383@qq.com>
| | Date:   Tue May 21 16:03:34 2024 +0800
| |
| |     Merge branch 'fix_B'
| |
| * commit 0b4a36e1391dd06fd95bd4487105e28b85ea44da (fix_B)
| | Author: Shiel <2910747383@qq.com>
| | Date:   Tue May 21 15:37:11 2024 +0800
| |
| |     Fix B
| |
* |   commit b90a352d988a418eb2a0ace9372b526291f36a4b
|\ \  Merge: d414820 125ae4f
| |/  Author: Shiel <2910747383@qq.com>
|/|   Date:   Tue May 21 15:33:04 2024 +0800
| |
| |       Merge branch 'feature_A'
| |
| * commit 125ae4f308db4709b575a5010d21a0ea7a4f762b (feature_A)
|/  Author: Shiel <2910747383@qq.com>
|   Date:   Tue May 21 15:30:40 2024 +0800
|
|       Add feature_A
|
* commit d41482024113f28391edc2e53576847f43feee87
| Author: Shiel <2910747383@qq.com>
| Date:   Tue May 21 15:28:04 2024 +0800
|
|     Add index
|
* commit 9f14bde42aae54c95919890c0567bdc6f40989ea
  Author: Shiel <2910747383@qq.com>
  Date:   Tue May 21 15:24:11 2024 +0800


xiluo@DESKTOP-AFIBLVR MINGW64 /f/WorkSpace/Github/git_tutorial (feature_C|REBASE 1/2)
$ vim README.md

xiluo@DESKTOP-AFIBLVR MINGW64 /f/WorkSpace/Github/git_tutorial (feature_C|REBASE 1/2)
$ git checkout -b feature_C
fatal: a branch named 'feature_C' already exists

xiluo@DESKTOP-AFIBLVR MINGW64 /f/WorkSpace/Github/git_tutorial (feature_C|REBASE 1/2)
$ vim README.md

xiluo@DESKTOP-AFIBLVR MINGW64 /f/WorkSpace/Github/git_tutorial (feature_C|REBASE 1/2)
$ git commit -am "Add feature_C"
[detached HEAD ef62a5e] Add feature_C
 1 file changed, 1 insertion(+)

xiluo@DESKTOP-AFIBLVR MINGW64 /f/WorkSpace/Github/git_tutorial (feature_C|REBASE 1/2)
$ vim README.md

xiluo@DESKTOP-AFIBLVR MINGW64 /f/WorkSpace/Github/git_tutorial (feature_C|REBASE 1/2)
$ git diff
diff --git a/README.md b/README.md
index 24a9eab..0794145 100644
--- a/README.md
+++ b/README.md
@@ -2,4 +2,4 @@

     - feature_A
     - fix_B
-    - faeture_C
+    - feature_C

xiluo@DESKTOP-AFIBLVR MINGW64 /f/WorkSpace/Github/git_tutorial (feature_C|REBASE 1/2)
$ git commit -am "Fix typo"
[detached HEAD 1a6614c] Fix typo
 1 file changed, 1 insertion(+), 1 deletion(-)

xiluo@DESKTOP-AFIBLVR MINGW64 /f/WorkSpace/Github/git_tutorial (feature_C|REBASE 1/2)
$ git rebase -i HEAD~2
fatal: It seems that there is already a rebase-merge directory, and
I wonder if you are in the middle of another rebase.  If that is the
case, please try
        git rebase (--continue | --abort | --skip)
If that is not the case, please
        rm -fr ".git/rebase-merge"
and run me again.  I am stopping in case you still have something
valuable there.


xiluo@DESKTOP-AFIBLVR MINGW64 /f/WorkSpace/Github/git_tutorial (feature_C|REBASE 1/2)
$ git rebase --abort

xiluo@DESKTOP-AFIBLVR MINGW64 /f/WorkSpace/Github/git_tutorial (feature_C)
$ git rebase -i HEAD~2
Auto-merging README.md
CONFLICT (content): Merge conflict in README.md
error: could not apply 0b4a36e... Fix B
hint: Resolve all conflicts manually, mark them as resolved with
hint: "git add/rm <conflicted_files>", then run "git rebase --continue".
hint: You can instead skip this commit: run "git rebase --skip".
hint: To abort and get back to the state before "git rebase", run "git rebase --abort".
hint: Disable this message with "git config advice.mergeConflict false"
Could not apply 0b4a36e... Fix B

xiluo@DESKTOP-AFIBLVR MINGW64 /f/WorkSpace/Github/git_tutorial (feature_C|REBASE 1/2)
$ git log
commit b90a352d988a418eb2a0ace9372b526291f36a4b (HEAD)
Merge: d414820 125ae4f
Author: Shiel <2910747383@qq.com>
Date:   Tue May 21 15:33:04 2024 +0800

    Merge branch 'feature_A'

commit 125ae4f308db4709b575a5010d21a0ea7a4f762b (feature_A)
Author: Shiel <2910747383@qq.com>
Date:   Tue May 21 15:30:40 2024 +0800

    Add feature_A

commit d41482024113f28391edc2e53576847f43feee87
Author: Shiel <2910747383@qq.com>
Date:   Tue May 21 15:28:04 2024 +0800

    Add index

commit 9f14bde42aae54c95919890c0567bdc6f40989ea
Author: Shiel <2910747383@qq.com>
Date:   Tue May 21 15:24:11 2024 +0800

    First commit

xiluo@DESKTOP-AFIBLVR MINGW64 /f/WorkSpace/Github/git_tutorial (feature_C|REBASE 1/2)
$ git log --graph
*   commit b90a352d988a418eb2a0ace9372b526291f36a4b (HEAD)
|\  Merge: d414820 125ae4f
| | Author: Shiel <2910747383@qq.com>
| | Date:   Tue May 21 15:33:04 2024 +0800
| |
| |     Merge branch 'feature_A'
| |
| * commit 125ae4f308db4709b575a5010d21a0ea7a4f762b (feature_A)
|/  Author: Shiel <2910747383@qq.com>
|   Date:   Tue May 21 15:30:40 2024 +0800
|
|       Add feature_A
|
* commit d41482024113f28391edc2e53576847f43feee87
| Author: Shiel <2910747383@qq.com>
| Date:   Tue May 21 15:28:04 2024 +0800
|
|     Add index
|
* commit 9f14bde42aae54c95919890c0567bdc6f40989ea
  Author: Shiel <2910747383@qq.com>
  Date:   Tue May 21 15:24:11 2024 +0800

      First commit

xiluo@DESKTOP-AFIBLVR MINGW64 /f/WorkSpace/Github/git_tutorial (feature_C|REBASE 1/2)
$ git rebase --abort

xiluo@DESKTOP-AFIBLVR MINGW64 /f/WorkSpace/Github/git_tutorial (feature_C)
$ git rebase --abort
fatal: no rebase in progress

xiluo@DESKTOP-AFIBLVR MINGW64 /f/WorkSpace/Github/git_tutorial (feature_C)
$ git log --graph
* commit 4d265a520a7a757f165ca5c3d91357bd00846859 (HEAD -> feature_C)
| Author: Shiel <2910747383@qq.com>
| Date:   Tue May 21 16:14:38 2024 +0800
|
|     Add feature_C
|
*   commit e57335cab86bb76985dbccfe4e4b331f41622e62 (master)
|\  Merge: b90a352 0b4a36e
| | Author: Shiel <2910747383@qq.com>
| | Date:   Tue May 21 16:03:34 2024 +0800
| |
| |     Merge branch 'fix_B'
| |
| * commit 0b4a36e1391dd06fd95bd4487105e28b85ea44da (fix_B)
| | Author: Shiel <2910747383@qq.com>
| | Date:   Tue May 21 15:37:11 2024 +0800
| |
| |     Fix B
| |
* |   commit b90a352d988a418eb2a0ace9372b526291f36a4b
|\ \  Merge: d414820 125ae4f
| |/  Author: Shiel <2910747383@qq.com>
|/|   Date:   Tue May 21 15:33:04 2024 +0800
| |
| |       Merge branch 'feature_A'
| |
| * commit 125ae4f308db4709b575a5010d21a0ea7a4f762b (feature_A)
|/  Author: Shiel <2910747383@qq.com>
|   Date:   Tue May 21 15:30:40 2024 +0800
|
|       Add feature_A
|
* commit d41482024113f28391edc2e53576847f43feee87
| Author: Shiel <2910747383@qq.com>
| Date:   Tue May 21 15:28:04 2024 +0800
|
|     Add index
|
* commit 9f14bde42aae54c95919890c0567bdc6f40989ea

xiluo@DESKTOP-AFIBLVR MINGW64 /f/WorkSpace/Github/git_tutorial (feature_C)
$ vim README.md

xiluo@DESKTOP-AFIBLVR MINGW64 /f/WorkSpace/Github/git_tutorial (feature_C)
$ git checkout master
Switched to branch 'master'

xiluo@DESKTOP-AFIBLVR MINGW64 /f/WorkSpace/Github/git_tutorial (master)
$ git merge --no-ff feature_C
Merge made by the 'ort' strategy.
 README.md | 1 +
 1 file changed, 1 insertion(+)

xiluo@DESKTOP-AFIBLVR MINGW64 /f/WorkSpace/Github/git_tutorial (master)
$ git remote add origin git@github.com:Akari2333/git_tutorial.git

xiluo@DESKTOP-AFIBLVR MINGW64 /f/WorkSpace/Github/git_tutorial (master)
$ git push -u origin master
Enumerating objects: 20, done.
Counting objects: 100% (20/20), done.
Delta compression using up to 12 threads
Compressing objects: 100% (9/9), done.
Writing objects: 100% (20/20), 1.57 KiB | 535.00 KiB/s, done.
Total 20 (delta 2), reused 0 (delta 0), pack-reused 0 (from 0)
remote: Resolving deltas: 100% (2/2), done.
To github.com:Akari2333/git_tutorial.git
 * [new branch]      master -> master
branch 'master' set up to track 'origin/master'.

xiluo@DESKTOP-AFIBLVR MINGW64 /f/WorkSpace/Github/git_tutorial (master)
$ git checkout -b feature_D
Switched to a new branch 'feature_D'

xiluo@DESKTOP-AFIBLVR MINGW64 /f/WorkSpace/Github/git_tutorial (feature_D)
$ git push -u origin feature_D
Total 0 (delta 0), reused 0 (delta 0), pack-reused 0 (from 0)
remote:
remote: Create a pull request for 'feature_D' on GitHub by visiting:
remote:      https://github.com/Akari2333/git_tutorial/pull/new/feature_D
remote:
To github.com:Akari2333/git_tutorial.git
 * [new branch]      feature_D -> feature_D
branch 'feature_D' set up to track 'origin/feature_D'.

xiluo@DESKTOP-AFIBLVR MINGW64 /f/WorkSpace/Github/git_tutorial (feature_D)
$ git branch
  feature_A
  feature_C
* feature_D
  fix_B
  master

xiluo@DESKTOP-AFIBLVR MINGW64 /f/WorkSpace/Github/git_tutorial (feature_D)
$ git remote -v
origin  git@github.com:Akari2333/git_tutorial.git (fetch)
origin  git@github.com:Akari2333/git_tutorial.git (push)

xiluo@DESKTOP-AFIBLVR MINGW64 /f/WorkSpace/Github/git_tutorial (feature_D)
$ git branch -a
  feature_A
  feature_C
* feature_D
  fix_B
  master
  remotes/origin/feature_D
  remotes/origin/master

xiluo@DESKTOP-AFIBLVR MINGW64 /f/WorkSpace/Github/git_tutorial (feature_D)
$ git branch master
fatal: a branch named 'master' already exists

xiluo@DESKTOP-AFIBLVR MINGW64 /f/WorkSpace/Github/git_tutorial (feature_D)
$ git checkout -
Switched to branch 'master'
Your branch is up to date with 'origin/master'.

xiluo@DESKTOP-AFIBLVR MINGW64 /f/WorkSpace/Github/git_tutorial (master)
$ git branch
  feature_A
  feature_C
  feature_D
  fix_B
* master

xiluo@DESKTOP-AFIBLVR MINGW64 /f/WorkSpace/Github/git_tutorial (master)
$ git branch -a
  feature_A
  feature_C
  feature_D
  fix_B
* master
  remotes/origin/feature_D
  remotes/origin/master

xiluo@DESKTOP-AFIBLVR MINGW64 /f/WorkSpace/Github/git_tutorial (master)
$ git pull origin feature_D
remote: Enumerating objects: 5, done.
remote: Counting objects: 100% (5/5), done.
remote: Compressing objects: 100% (2/2), done.
remote: Total 3 (delta 0), reused 3 (delta 0), pack-reused 0
Unpacking objects: 100% (3/3), 261 bytes | 6.00 KiB/s, done.
From github.com:Akari2333/git_tutorial
 * branch            feature_D  -> FETCH_HEAD
   6d44a12..ff1d843  feature_D  -> origin/feature_D
Updating 6d44a12..ff1d843
Fast-forward
 README.md | 1 +
 1 file changed, 1 insertion(+)
```





# 2 git_tutorial dev

```bash

xiluo@DESKTOP-AFIBLVR MINGW64 /f/WorkSpace/Github/git_tutorial dev
$ git clone git@github.com:Akari2333/git_tutorial.git
Cloning into 'git_tutorial'...
remote: Enumerating objects: 20, done.
remote: Counting objects: 100% (20/20), done.
remote: Compressing objects: 100% (7/7), done.
remote: Total 20 (delta 2), reused 20 (delta 2), pack-reused 0
Receiving objects: 100% (20/20), done.
Resolving deltas: 100% (2/2), done.

xiluo@DESKTOP-AFIBLVR MINGW64 /f/WorkSpace/Github/git_tutorial dev
$ git branch -a
fatal: not a git repository (or any of the parent directories): .git

xiluo@DESKTOP-AFIBLVR MINGW64 /f/WorkSpace/Github/git_tutorial dev
$ git init
Initialized empty Git repository in F:/WorkSpace/Github/git_tutorial dev/.git/

xiluo@DESKTOP-AFIBLVR MINGW64 /f/WorkSpace/Github/git_tutorial dev (master)
$ git branch -a

xiluo@DESKTOP-AFIBLVR MINGW64 /f/WorkSpace/Github/git_tutorial dev (master)
$ git branch -a

xiluo@DESKTOP-AFIBLVR MINGW64 /f/WorkSpace/Github/git_tutorial dev (master)
$ ^C

xiluo@DESKTOP-AFIBLVR MINGW64 /f/WorkSpace/Github/git_tutorial dev (master)
$ git branch -r

xiluo@DESKTOP-AFIBLVR MINGW64 /f/WorkSpace/Github/git_tutorial dev (master)
$ git branch -r

xiluo@DESKTOP-AFIBLVR MINGW64 /f/WorkSpace/Github/git_tutorial dev (master)
$ git branch -a

xiluo@DESKTOP-AFIBLVR MINGW64 /f/WorkSpace/Github/git_tutorial dev (master)
$ git remote -v

xiluo@DESKTOP-AFIBLVR MINGW64 /f/WorkSpace/Github/git_tutorial dev (master)
$ git remote add origin git@github.com:Akari2333/git_tutorial.git

xiluo@DESKTOP-AFIBLVR MINGW64 /f/WorkSpace/Github/git_tutorial dev (master)
$ git fetch origin
remote: Enumerating objects: 20, done.
remote: Counting objects: 100% (20/20), done.
remote: Compressing objects: 100% (7/7), done.
remote: Total 20 (delta 2), reused 20 (delta 2), pack-reused 0
Unpacking objects: 100% (20/20), 1.55 KiB | 6.00 KiB/s, done.
From github.com:Akari2333/git_tutorial
 * [new branch]      feature_D  -> origin/feature_D
 * [new branch]      master     -> origin/master

xiluo@DESKTOP-AFIBLVR MINGW64 /f/WorkSpace/Github/git_tutorial dev (master)
$ git branch -a
  remotes/origin/feature_D
  remotes/origin/master

xiluo@DESKTOP-AFIBLVR MINGW64 /f/WorkSpace/Github/git_tutorial dev (master)
$ git remote -v
origin  git@github.com:Akari2333/git_tutorial.git (fetch)
origin  git@github.com:Akari2333/git_tutorial.git (push)

xiluo@DESKTOP-AFIBLVR MINGW64 /f/WorkSpace/Github/git_tutorial dev (master)
$ git branch -a
  remotes/origin/feature_D
  remotes/origin/master

xiluo@DESKTOP-AFIBLVR MINGW64 /f/WorkSpace/Github/git_tutorial dev (master)
$ git remote add origin git@github.com:Akari2333/git_tutorial.git
error: remote origin already exists.

xiluo@DESKTOP-AFIBLVR MINGW64 /f/WorkSpace/Github/git_tutorial dev (master)
$ git fetch origin

xiluo@DESKTOP-AFIBLVR MINGW64 /f/WorkSpace/Github/git_tutorial dev (master)
$ git branch -a
  remotes/origin/feature_D
  remotes/origin/master

xiluo@DESKTOP-AFIBLVR MINGW64 /f/WorkSpace/Github/git_tutorial dev (master)
$ git branch

xiluo@DESKTOP-AFIBLVR MINGW64 /f/WorkSpace/Github/git_tutorial dev (master)
$ git checkout -b feature_D origin/feature_D
Switched to a new branch 'feature_D'
branch 'feature_D' set up to track 'origin/feature_D'.

xiluo@DESKTOP-AFIBLVR MINGW64 /f/WorkSpace/Github/git_tutorial dev (feature_D)
$ ls
README.md  git_tutorial/

xiluo@DESKTOP-AFIBLVR MINGW64 /f/WorkSpace/Github/git_tutorial dev (feature_D)
$ vim README.md

xiluo@DESKTOP-AFIBLVR MINGW64 /f/WorkSpace/Github/git_tutorial dev (feature_D)
$ git diff
diff --git a/README.md b/README.md
index 0794145..7ae6730 100644
--- a/README.md
+++ b/README.md
@@ -3,3 +3,4 @@
     - feature_A
     - fix_B
     - feature_C
+    - feature_D

xiluo@DESKTOP-AFIBLVR MINGW64 /f/WorkSpace/Github/git_tutorial dev (feature_D)
$ git commit -am "Add feature_D"
[feature_D ff1d843] Add feature_D
 1 file changed, 1 insertion(+)

xiluo@DESKTOP-AFIBLVR MINGW64 /f/WorkSpace/Github/git_tutorial dev (feature_D)
$ git push
Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Delta compression using up to 12 threads
Compressing objects: 100% (2/2), done.
Writing objects: 100% (3/3), 281 bytes | 281.00 KiB/s, done.
Total 3 (delta 0), reused 0 (delta 0), pack-reused 0 (from 0)
To github.com:Akari2333/git_tutorial.git
   6d44a12..ff1d843  feature_D -> feature_D

xiluo@DESKTOP-AFIBLVR MINGW64 /f/WorkSpace/Github/git_tutorial dev (feature_D)
$ ^C

xiluo@DESKTOP-AFIBLVR MINGW64 /f/WorkSpace/Github/git_tutorial dev (feature_D)
$

```

