# just-started
This is my first git repo and am learning to understand the git and github .

In Github
Commit is a 2 step process
- the `commit` --> means the changes jo bi kiya usko tho pakka kar raha hai
- after every commit , git stores the info ( saves ur commit ) and the date you commit
- in order to change --> you `add` ( a change ) and then commit

**Clone** 
- copy the link to clone from code dropdown of the git repo
- create new folder and type `git clone [paste ur link here]`
- your git repo get's cloned into the folder

**Commands**
- `cd just-started` moves ur directory to ur repository [ just-started is the name of my repo, you have to type ur name there or use autotype]
- `ls` it bascially shows the list of files in ur repo or in that directory
- `ls -Hidden` shows hidden files, every git integrated file has `.git` folder to track ur changes

**Status**
- `git status` it shows on what brach you are on and shows if you have saved or not saved ur file [ save --> commit ]

We have **4 types of status** 
1. `untracked` --> new files that **git doesn't yet track**, even if you modify the file or add new stuff. If it is **newly added externally** from git then it is untracked
2. `modified` --> Files that already exist but are modified/changed
3. `unmodifed` --> Files that already exist but are unchanged
4. `staged` --> 
- after you `add` ur changed code then that becomes staged code 
- something that is ready to `commit`

To Track changes , git uses 2 commands
1. `add`
2. `commit`

**Add**
- Adds new or changed files in your working directory to the Git staging area

[Staging area --> It's the area where the unmodified and untracked files exist]

To add single files:-
*syntax* --> `git add <-file name->`

To add all files:-
*syntax* --> `git add .`

**Commit** 
- It is the record of the change
*syntax* --> `git commit -m "some message"`
here `-m` means your commit has some message

what you have saved now , won't show on the github page as it is locally saved in ur laptop

so to resolve this issue you have to

**PUSH**
- upload local repo content to remote repo

[
    **Local repo** - the repository is saved in ur laptop or pc 
    **Remote repo** - the repository is saved in the github
]

*syntax* --> `git push origin main`

So what does this syntax mean

By default , all the repositories of github, those are called remote repos
Among those repos we choose one default repo , through which we can clone our code
Which means on pushing, our code gets pushed to that default repo and that default repo's name is `origin`

`main` 
It is the branch name. In what branch our `origin` repo exists.

We can also use 
`git push -u origin main` 
now what does this `-u` mean
It means to set upstream
which means when you are working on a project for long time and for acd ll the time you are pushing to origin main
then you can use this command to automate it

so next time all you have to do is type
`git push` and your code gets pushed to origin main


**Init Command**
- used to create a new git repo 
- like when you build a project or write a simple code file in your computer but now you want to upload to git then this is used

*syntax* --> `git init`

Now to add new repo in github from local we use
`git remote add origin <-link->`
and the name of the file place is origin
by default we keep origin as it is widely used

To check to what remote repo have we added our file use
`git remote -v`

**WorkFlow of Github**
1. Creation of github repository [ remote file ] 
2. `clone` the repo into local file
3. Changes made in the code
[ do not forget to save the files in vs code or else the changes will not be noted in the terminal ]
4. `add`
5. `commit`
6. `push`

**Branch** 
- for suppose there are 3 teams
1. frontend 
2. Backend
3. Bug fix

There will be a main branch
Each team will take their own branches from the main branch
And from which point they take, from that point onwards they get a copy of the code/repo

<img title="Git_Branches" alt="Git Branches pic" src="/just-started/GIt_Branches.png">

This tree like looking structure is called **Working Tree**

`git branch` --> to check on what branch you are on

To Rename your git branch 
`git branch -M newName`

To Move to another branch
`git checkout <-branch name->`

To Create New Branches 
`git checkout -b <-new branch name->`

To Delete Branches
`git checkout -d <-new branch name->`

**Merging Code**
Using Terminal->
1. `git diff <-branch name->`
This is to compare the code from the branch that you are in and the branch name you want to check with

This would give you each change that happened , even tiny details

Sometimes ur terminal would run a code infintely [END] with something like this at the end, then just press `q` and it will stop the infite operation from happening and return to ur terminal input

2. `git merge <-branch-name->`
This is to merge 2 branches
When 2 branches code becomes the same then you can merge them

Using Github->
1. Create a **PR**
**PR** means a *Pull request*
It lets you tell others about the changes you've pushed to a branch in a repository on GitHub

Let's say a lot of people are woring on a single project and all of them wants to merge with the main then they pull this pull request

So when you do this, The main branches Senior developer [could be anyone but here for instance] , they will review your code --> this is called **PR Review** and comment over it.

**PULL COMMAND**
Used to fetch and download content from a remote repo and immediately update the local repo to match the content

`git pull origin main`

**Resolving Merge Conflicts**
An event that takes place when Git is unable to automatically resolve the differnences in code between two commits

In simple words
When the code in one branch differs from the code in other branch , like same sentence but different wording, for suppose

```html
<p>New repo created</p>
<p>This is a new feature [button]</p>
```
This is from main branch

```html
<p>New repo created</p>
<p>This is a new feature [dropdown]</p>
```
This is from feature1 branch

Then git won't be able to tell which commit should it commit, heh get the pun
sorry about my humor but anyway

Git wouldn't know what to save and merge, this causes merge conflicts

To Resolve these conflicts 
VS Code being a smart editor suggests resolutions
Incoming change --> changes that are coming from main branch
Current change --> changes from our feature1 branch
