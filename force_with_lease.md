## Force With Lease Lab
1. Adding for first commit
2. Adding for second commit

### Rebase Observations
Before rebase :-

5225e3b first small commit

47513de (HEAD -> force-lease-lab, origin/force-lease-lab) second small commit

After Rebase :-

342c452 first small commit

4344044 (HEAD -> force-lease-lab) second small commit

So the hash codes for the commits changed after the rebase and also, the simple git push won't work in this case. That is the reason why we use fetch with lease so that our rebase can be pushed successfully. A standard `--force` push blindly overwrites the remote branch and can instantly delete a teammate's newly pushed work. `--force-with-lease` checks the remote repository first, if someone else has added commits that we haven't pulled down yet, it safely aborts the push to protect their work.