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

**Init Command**
- used to create a new git repo 
- like when you build a project or write a simple code file in your computer but now you want to upload to git then this is used

