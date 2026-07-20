## Some Important commands and outputs :-

1. Command :- git log --oneline
Output :-
4b4c127 (HEAD -> capstone-conflict) Add incorrect line in programs.md file
1c85751 (origin/capstone-conflict) Add capstone conflict progress entry
d41747e (origin/develop) Merge pull request #33 from Krish-Mishra/capstone-feature
c33a141 (origin/capstone-feature, capstone-feature) Add capstone feature progress entry
e3d5784 Add useful lessons
b5a1536 (develop) Merge pull request #32 from Krish-Mishra/add-pages-link
345c0bd (origin/add-pages-link, add-pages-link) Add live page link to README file
727ec26 Merge pull request #30 from Krish-Mishra/profile-page
d0083ae (origin/profile-page, profile-page) Add profile info file
27b9cdd Merge pull request #29 from Krish-Mishra/summary-docs
c7e7b1a (origin/summary-docs, summary-docs) Add merge strategies corrected summary file
caa8e69 Add merge strategies summary file
a8b8ca9 Add second rebase strategy commit
be74832 Add first rebase strategy commit
3338df1 Squash demo (#27)
60975e3 Merge pull request #26 from Krish-Mishra/merge-commit-demo

2. Command :- git revert --no-edit 4b4c127
Output :-
[capstone-conflict 09e9f00] Revert "Add incorrect line in programs.md file"
 Date: Mon Jul 20 23:49:19 2026 +0530
 1 file changed, 1 insertion(+), 3 deletions(-)

3. Command :- git cherry-pick e4e77e8
Output :-
[capstone-feature e3d5784] Add useful lessons
 Date: Mon Jul 20 23:35:25 2026 +0530
 1 file changed, 3 insertions(+)
 create mode 100644 journal/git_lessons.md

 4. Command :- git rebase origin/develop
 Output :-
 Auto-merging README.md
CONFLICT (content): Merge conflict in README.md
error: could not apply 13df8eb... Add capstone conflict progress entry
hint: Resolve all conflicts manually, mark them as resolved with
hint: "git add/rm <conflicted_files>", then run "git rebase --continue".
hint: You can instead skip this commit: run "git rebase --skip".
hint: To abort and get back to the state before "git rebase", run "git rebase --abort".
hint: Disable this message with "git config set advice.mergeConflict false"
Could not apply 13df8eb... # Add capstone conflict progress entry

5. Command :- git rebase --continue
Output :-
[detached HEAD 1c85751] Add capstone conflict progress entry
 1 file changed, 2 insertions(+)
Successfully rebased and updated refs/heads/capstone-conflict.

6. Command :- git push -u origin capstone-conflict --force-with-lease
Output :-
Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Delta compression using up to 8 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 361 bytes | 361.00 KiB/s, done.
Total 3 (delta 2), reused 0 (delta 0), pack-reused 0 (from 0)
remote: Resolving deltas: 100% (2/2), completed with 2 local objects.
remote: 
remote: Create a pull request for 'capstone-conflict' on GitHub by visiting:
remote:      https://github.com/Krish-Mishra/KrishGitPractice/pull/new/capstone-conflict
remote: 
To github.com:Krish-Mishra/KrishGitPractice.git
 * [new branch]      capstone-conflict -> capstone-conflict
branch 'capstone-conflict' set up to track 'origin/capstone-conflict'.