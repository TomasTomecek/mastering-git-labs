# Mastering git: class 2 lab

## Class 2 topics

* Branches
* Tags
* Merging
* Stash


## Lab

### Setup

* Clone this repository (clone it again even if you have a copy locally)
  * Run `git branch add-lab-description origin/add-lab-description`
  * Run `git branch wip-show-sample-commands origin/wip-show-sample-commands`
  * These commands will create local copies of branches from remote origin: in this repository

### Tasks

* Delete branch “wip-show-sample-commands”
* Does the “add-lab-description” top commit look okay?
  * Fix the problem once you spot it
* Create a new branch that starts from "add-lab-description", name it “fix”
* Oh, that’s not a good branch name, sorry. Rename the branch from “fix” to “fix-add-lab-description”
* Merge fix-add-lab-description into main
* BONUS: push your local main into your fork
* EPIC BONUS: Create a pull request from fix-add-lab-description to this repository
