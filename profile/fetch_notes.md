## Fetch Notes

* Fetch is similar to pull.
* It may have some advantage over the pull command.
* I guess it works on layered pull for safety.\

## What Fetch Showed Me

1. git status

Output :-
On branch fetch-practice
Your branch is behind 'origin/fetch-practice' by 1 commit, and can be fast-forwarded.
  (use "git pull" to update your local branch)

nothing to commit, working tree clean

2. git log HEAD..origin/fetch-practice --oneline 

Output :- 
db94fd5 (origin/fetch-practice) Update fetch_notes.md with additional bullet point

3. git diff HEAD..origin/fetch-practice

Output :-
diff --git a/profile/fetch_notes.md b/profile/fetch_notes.md
index 1fb099d..30640fa 100644
--- a/profile/fetch_notes.md
+++ b/profile/fetch_notes.md
@@ -2,4 +2,5 @@
 
 * Fetch is similar to pull.
 * It may have some advantage over the pull command.
-* I guess it works on layered pull for safety.
\ No newline at end of file
+* I guess it works on layered pull for safety.
+* This bullet point is added through GitHub UI.