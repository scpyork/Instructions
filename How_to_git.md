# Github

First set up an account on www.github.com


### Installation
#### Windows:
  Download and run from: https://gitforwindows.org/
#### Mac:
  Open terminal, `brew install git`
#### Linux:
  Open terminal, `sudo apt-get (or equivaent) install git`



## Usage
Open Terminal or GitBash (windows)  - reffered to as console for the purposes of this script

### Simple bash commands
`ls` - lists files in directory 

`pwd` - current home directory

 `cd <directory>` - change directory
 
 `mv <file from> <file to>` move
 
 `cp <file from> <file to>` copy
 
 
 ## Add credentials 
  
```
git config --global user.name "MyName"
git config --global user.email "hi@sei.org"
```
 
 
 ## Create a new Repository
 Easiest done online, `https://github.com/ <yourusername> /repositories/new` ?
 - Make sure you select make with README
 
## Downloading an existing, or newlymade repository
` git clone https://github.com/scpyork/faostat-pull.git`

## Branches
You can have a series of branches from people working on the same project but dont want to override the main code. 
These are easily merged back in using the web interface. 

## Selecting a branch
`git checkout -b <branchname>`


## Saving changes
` git add -A` - Adds any new files to be tracked
` git commit -m 'Here are the changes I made today <commit message>`

## Upload changes online
`git push origin <branchname, or master`

## Pull any changes from the last time you used the code. This merges your changes with the updates. 
`git pull`




## Large file problems
Git can only store files online <100mb as a default. See git-large etc for other files/data. This is fine for code etc, although may cause problems when you accidentally commit a large file and try to push a repository (even if you delete the file). 
The following script tends to work for me in most cases in fixing this

`git filter-branch -f --index-filter "git rm -r --cached --ignore-unmatch $@" HEAD `


 
 
 
 
 
 ## Cheatsheet
 https://docs.google.com/viewer?url=https%3A%2F%2Fwww.atlassian.com%2Fdam%2Fjcr%3A8132028b-024f-4b6b-953e-e68fcce0c5fa%2Fatlassian-git-cheatsheet.pdf
