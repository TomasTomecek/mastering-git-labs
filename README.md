# Mastering git: class labs


## Class 4


## Class 3

* Push & pull
* Remotes
* Pull requests

### Lab

* find a file with your `<UCO>.txt` and write down what’s the most valuable thing you learnt so far on this course
* CI needs to pass
* BONUS: contribute also to `what_we_learnt.txt` (beware of rebase and merge conflicts!)


## Class 2

* Branches
* Tags
* Merging
* Stash

### Lab

#### Setup

* Clone this repository (clone it again even if you have a copy locally)
  * Run `git branch add-lab-description origin/add-lab-description`
  * Run `git branch wip-show-sample-commands origin/wip-show-sample-commands`
  * These commands will create local copies of branches from remote origin: in this repository

#### Tasks

* Delete branch “wip-show-sample-commands”
* Does the “add-lab-description” top commit look okay?
  * Fix the problem once you spot it
* Create a new branch that starts from "add-lab-description", name it “fix”
* Oh, that’s not a good branch name, sorry. Rename the branch from “fix” to “fix-add-lab-description”
* Merge fix-add-lab-description into main
* BONUS: push your local main into your fork
* EPIC BONUS: Create a pull request from fix-add-lab-description to this repository

### Solution

You are still free to do this task.

<details>
  <summary>Click only when you want to see the solution for this lab with the explanation for commands.</summary>

  1. Delete the branch: `git branch -D wip-show-sample-commands` (has to be `-D` since the branch is not merged).
  2. `git switch add-lab-description`, let's work on the "add-lab-description" branch.
  3. There is a typo in README.md, we can fix it easily: `workflowwwwwwwwwwwwwwwwwwwwww` → `workflow`.
  4. `git commit -a -m 'fix typo in readme'` - we want to preserve the original commit.
  5. `git switch -c fix`: instructions say to create this branch.
  6. Uhhhh, make your mind! 😄 `git branch -m fix fix-add-lab-description`
  7. `git switch main && git merge fix-add-lab-description`: merged, sweet!
  8. In order to push, we need to set up our fork remote, but let's do this properly:

   * `git remote rename origin upstream`: we want our for to be the default and the actual upstream repo to be named "upstream"
   * `git remote add origin git@github.com:$USERNAME/mastering-git-class2-lab`: now to set up our fork
   * `git fetch --all`: let's fetch all refs to be sure we set it up correctly

  9. Let's push to our fork's main to see our change: `git push origin main:main` (we are telling git to push our local branch `main` into our fork repository and name the branch `main` there: so basically put our new local commits from main into fork's main)
  10. The best practice is to create pull requests from dedicated branches, not main, so let's push again: `git push origin fix-add-lab-description:fix-add-lab-description`
  11. Time to create the PR!

</details>

Did you find a problem? Something doesn't work? Please ask or contribute a fix.
