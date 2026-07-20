# Git Inspection History

### 1. `git status`
**Output:**
On branch inspection-extra
Your branch is up to date with 'origin/inspection-extra'.

Untracked files:
  (use "git add <file>..." to include in what will be committed)
        inspection/history.md

nothing added to commit but untracked files present (use "git add" to track)
**My Answer:** I am on the 'inspection-extra' branch and the working tree is not clean because 'history.md' file is still untracked.

### 2. `git branch`
**Output:**
  develop
* inspection-extra
  inspection-practice
  main
**My Answer:** There are four local branches present which are :- develop, inspection-extra, inspection-practice and main.

### 3. `git branch -r`
**Output:**
  origin/HEAD -> origin/main
  origin/develop
  origin/inspection-extra
  origin/inspection-practice
  origin/main
**My Answer:** The remote branches which exist are :- main, develop, inspection-practice and inspection-extra. The origin/HEAD points to the default remote branch, which is 'main'.

### 4. `git branch -a`
**Output:**
  develop
* inspection-extra
  inspection-practice
  main
  remotes/origin/HEAD -> origin/main
  remotes/origin/develop
  remotes/origin/inspection-extra
  remotes/origin/inspection-practice
  remotes/origin/main
**My Answer:** Here we can see both the local and remote branches being listed as the output of the command. The key difference between them is that local branches are present only in our machine while remote branches are visible in our GitHub. also each remote branch had origin/ convention which signifies that these are essentially read only bookmarks.

### 5. `git log --oneline`
**Output:**
98a5a89 (HEAD -> inspection-extra, origin/inspection-extra) add extra inspection notes
b23f33c (origin/develop, develop) Added Introductory Readme file
e98ed11 Initial commit
**My Answer:** There are total 3 commits listed in the output, First and second commit come from develop branch as this branch is derived from it and the third commit is for the addition of 'extra.md' file.

### 6. `git log --oneline --decorate --graph --all`
**Output:**
* 98a5a89 (HEAD -> inspection-extra, origin/inspection-extra) add extra inspection notes
| * e8b2787 (origin/inspection-practice, inspection-practice) add inspection practice notes
|/  
| *   4be5a45 (origin/main, origin/HEAD, main) Merge pull request #1 from Krish-Mishra/develop
| |\  
| |/  
|/|   
* | b23f33c (origin/develop, develop) Added Introductory Readme file
|/  
* e98ed11 Initial commit
**My Answer:** Here we can see that, the branch has split for the commits 98a5a89 and e8b2787 which signifies that these are the commits from different branches. Also after the initial commit in main, we can see that the next commit is done on the develop branch and it got merged after into the main branch.

### 7. `git diff develop..inspection-extra`
**Output:**
diff --git a/inspection/extra.md b/inspection/extra.md
new file mode 100644
index 0000000..41d58f6
--- /dev/null
+++ b/inspection/extra.md
@@ -0,0 +1,5 @@
+## Extra Inspection Notes
+
+* Bullet point A.
+* Bullet point B.
+* Bullet point C.
\ No newline at end of file
**My Answer:** Compared to the develop branch, this branch adds a new file named 'inspection/extra.md' that contains the "Extra Inspection Notes" heading and three bullet points.

### 8. `git diff develop..inspection-practice`
**Output:**
diff --git a/inspection/notes.md b/inspection/notes.md
new file mode 100644
index 0000000..789e554
--- /dev/null
+++ b/inspection/notes.md
@@ -0,0 +1,5 @@
+## Inspection Notes
+
+* This is the first bullet point.
+* This is the second bullet point.
+* This is the third bullet point.
\ No newline at end of file
**My Answer:** This branch is different from 'inspection-extra' because it contains 'notes.md' file inside the inspection folder and the content inside it is also different.

### 9. `git show 98a5a89`
**Output:**
commit 98a5a898ecee8f9d741e841d81bda201ff15e0d8 (HEAD -> inspection-extra, origin/inspection-extra)
Author: Krish Mishra <rm25101980@gmail.com>
Date:   Thu Jul 9 18:37:32 2026 +0530

    add extra inspection notes

diff --git a/inspection/extra.md b/inspection/extra.md
new file mode 100644
index 0000000..41d58f6
--- /dev/null
+++ b/inspection/extra.md
@@ -0,0 +1,5 @@
+## Extra Inspection Notes
+
+* Bullet point A.
+* Bullet point B.
+* Bullet point C.
\ No newline at end of file
**My Answer:** In case of this commit with message 'add extra inspection notes', we added a new file named 'extra.md' in the inspection folder which has a heading and three bullet points added inside it. This commit was done in 'inspection-extra' branch.