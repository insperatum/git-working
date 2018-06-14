# git-working
Scripts for developing + running experiments with git in the loop.  
Every launched experiment is executed from its own folder, and tied to its own git commit in a working branch.

## Workflow
1. Initialise a working branch with `g-working`

2. Do some programming. Whenever you want to launch an experiment:
```sh
git add <files> #Add any new files
[name=<experiment name>] g-run <command> #e.g: name=linear_model g-run sbatch --time=60 run.sh
```

3. Merge changes into master:
```sh
g-master
git add <files>
git commit <args>
g-push #push to master, then move back to working branch
```  

4. Goto step 2
