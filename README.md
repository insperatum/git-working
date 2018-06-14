# git-working
Scripts for developing + running experiments with git in the loop.  
Every launched experiment is executed from its own folder, and tied to its own git commit in a working branch.

## Usage
1. Clone this repo and add it to your `$PATH`

2. Inside a git project, initialise a working branch with `g-working`

3. Do some programming. Whenever you want to launch an experiment:
```sh
git add <files> #Add any new files
[name=<experiment name>] g-run <command> #e.g: name=linear_model g-run sbatch --time=60 run.sh
```

4. Merge changes into master:
```sh
g-master
git add <files>
git commit <args>
g-push #push to master, then move back to working branch
```  

5. Goto step 3
