# git-working
Save/run concurrent experiments with git

(1) Move to working branch: `g-working`

(2) Launch experiment:
```
git add ... //anything new
g-run sbatch ...//
```

(3) Commit changes to master:
```
g-master
<Commit anything>
g-push
```
