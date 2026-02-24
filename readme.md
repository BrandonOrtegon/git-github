# Git Lesson
- version control systemn created by Linus Torvalds in 2005
- allows multiple developers to contribute to the same codebase
- That codebase or project is called a repository (repo for short)

## First Time Git Setup
- to see your git config, use the command `git config --global --list`
- to set your username, use `git config user-name "first last"`
- to set your email, use `git config user.email "email@here.com"`

## How to use Git
- **in the folder in which you intend to create a project** initialize a new git repository
- initialize a new repository using `git init` command
- in order to track files, use `git add <name of file>` to track a file
    - if you want to add all of the files at once, use `git add . `
- if you would like to unstage a file, you can use `git rm --cached <name of file>` to do so
- if you are ready to commit, use the `git commit -m "your commit mesage here"` command
> [!TIP]
> commit messages should succintly explain your changes
- `git log` will show you a history of your commits
- use `git add <file>...` to update what will be committed
- use `git restore <file>...` to discard changes in working directory

## Git Lingo
- branch - a timeline of your code at any given point
- the default branch is called the `main` branch or `master`
- commit - a snapshot of your code at a specific point in time

## Git Stages
- [ ] tracking
    - a way for us to decide which files git will track in its repository
- [ ] staging
    - a way for us to decide what will become a commit
- [ ] committing

## Git Log Explained
- commit hash - unique value describing our commit
- main/master (or other) - name of the branch on which the commit resides
- HEAD - think of this as eyes. It points to what our eyes are looking at
- author of the commit
- date the commit occurred
- commit message
- to get out of of it, you may need to hit `q`


## Connecting Git Repo to GitHub Repo
- create a repository on GitHub
    - sign in to GitHub with your cedentials
    - find the green `new` button to create a new repository
    - give it a repository name
    - choose visibility (usually public)
    - click `create repository`
- copy the HTTPS (or SSH if your setup requires it) link to your repo
- run the following command `git remote add origin <paste your link here>`
    - `remote` is responsible for remote repos
    - `add` adds something
    - `origin` this is the name we will give our remote repo to reference later. Commonly use origin or upstream.
    - `<your link>` is the HTTPS or SSH endpoint from the GitHub repo
- return back to syntax is a good thing!
- to verify it's successfully linked, run `git remove -v` to see the endpoint
- you should see the following:
    - name of the endpoint
    - the endpoint itself
    - fetch (bring down) and push (send up)
- in order to push your code, run `git push origin <name of branch>` (ex: `git push origin main`)


## Branches
Git allows you to create branches or alternate timelines. They allow you to create an exact 'Copy' of another branch. This way you can tinker with the code without affecting the original code. Great for building features without 'butting heads' with other developers on the project.


- `git branch` to check which branch you're in
- to create a new branch:
    - `git branch <name of your branch>`
    - then you have to go to this branch using `git checkout <name of your branch>`
> [!TIP}]
> two in one! create a new branch and checkout all at once by using: 
> `git checkout -b <name of your branch>` (ex: `git checkout -b develop`)
- it should say 'switched to a new branch 'name of your branch''
- this change is now exclusively on develop branch
- you can see it by running `git checkout main` or `git checkout develop`.