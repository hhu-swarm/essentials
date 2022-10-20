# Git

Git is a version control system.

## Advantages
- Keep & manage multiple versions of code
- Share code between multiple people with following advantages:
    - code version and source is always transparent
    - code, that originated from the same codebase, is easily merged together, whenever 2 developer create new code versions parrallelly
- code is always stored in a central repository, that allows for
    - data security (scripts dont get lost)
    - communication with central repository always happens equivalently. 

## Vocabulary


### Nouns

`git` is a version control system.

`github` is a website and much more

a git `repository` is a storage location for all possible versions of someones codebase. It might be located on e.g. github as a bare repository or on your current device as a working (or live) repository

a `branch` is tracking a specific codebase and all of its historic versions

a `commit` is a command for creating a timestamp and versionstamp of a codebase

a `codebase` is the accumulation of all scripts and small assets belonging to project

`remote` or origin is a (often) central git repository like your project repository on github

### Verbs

to `checkout` a branch means activating the current state of a branch. This is the state of the lastest commit of a branch. This command will **remove** all contents from your current working directory and replace its contents with said state.

`adding` something to your repository will include a new file, that was not previously beeing tracked

`pushing` changes means uploading all newly created commits to your origin

`merging` branch A with branch B means combining their states and saving the result into branch A 

### Adjectives

being `a´HEAD` means being checked out to the latest version of a repositories codebase

being `tracked` are all files that get commited, whenever you do so. Files are not tracked if they are either ignored or `untracked` (not yet tracked)

A file is `ignored` if it matches the patterns within a `.gitignore` file in the current or a (direct/indirect) parent directory

a `bare` repository contains no checkout functionality as all data is stored in there in binary format

## Commands

### Initialize new repository
`git init`

### Clone
`git clone <repository url>`

### Commit
`git commit -m "<message>"`

### Push new commits
`git push <remote> <repote branch>`

### Adding new files to git tracking
`git add .` *(in project root directory)*

### Checking out a new branch
`git checkout <branch>`

### Create new branch from current branch
`git checkout -b <name>`

### Merge
`git merge <other branch>`


## Common workflow elements

There are hundreds of different possible workflows. Following is a list of steps required to successfully contribute to a project.


### Creation
Those steps assume the central repository to be hosted on Github.com
- Clone an existing repository
- Create a new branch from *main* branch
    - Whenever you try to fix something: call it **fix_issueID** where *issueID* identifies an existing Github Issue Item. 
    - Otherwise call it **feature_featureTitleOrIssueID** 
- Make your changes in the codebase now
- Commit your changes step by step. Comit as soon as you changed a significant portion of code, that is easily explained using very few (5-10) words. Do not make more changes than that without committing and explaining your change in your commit message.
- Rense and repeat until your issue is fixed **and** successfully tested or your feature is **fully** implemented
- **push** your issue- or feature-branch to github regulary, as this allows others to help fixing the issue or implementing the feature without needing to start over again.

### Integration
In order to integrate your changes into a environment branch, you will need to merge both of them together
- Checkout the respective environment branch
- Merge your branch into this enviroment branch
- fix possible merge conflicts
- commit during this process whenever you changed something meaningful
- commit after fixing all merge conflicts
- push the environment branch to github
- now its time to create a pull request on github. This will ensure your changes are going to be **integrated** into the main (or testing/staging/production) branch
- Your pull request will need to be approved by other members, who are capable to review your changes
    - If your request is declined, you will need to improve your changes. You`ll find a list of suggestions attached to the declined request 
    - If your request is approved, it is integrated into the respective environment branch