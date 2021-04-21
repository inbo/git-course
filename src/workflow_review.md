---
description: "Git workflow for collaboration"
title: Workflow Collaboration
output:
  html_document:
    toc: true
    toc_depth: 2
    toc_float: true
---

These guidelines explain the different steps to be taken when collaborating
in a Github repository while developing code in RStudio. The main aim is to
give a concise overview rather than giving detailed information on different
options or showing screenshots for each step. The steps presented here follow
more or less [this schedule](https://guides.github.com/introduction/flow/) but
the explanations and tips are rather complementary.

# Add an issue

Ask for changes or propose to make changes in a Github repository:

- on the main page of the git repository on GitHub, hit tab `Issues`
- check for similar issues (using the search function)
    - if the issue already exists, add your comments or suggestions in this issue, or add a thumb emoticon (to follow the issue)
- if your issue is not yet reported, hit the button `New issue`
- give it an informative title and add a clear and complete description (with reproducible example if appropriate)

Issues can be used to:

- report to do's to yourself/team
- propose and discuss additions/changes
- report bugs in packages you're using

Issues can be:

- assigned to someone
- labeled (e.g. bug, documentation, help wanted,...)

# Add code in a new feature branch

(If you don't have the project locally, check the manual [here](https://inbo.github.io/git-course/course_rstudio.html#23_clone_a_repo_to_work_locally).)

In RStudio on the `Git`tab:

- make sure the `master` branch is active and up to date (`Pull`)
- add a `New Branch` (hit button) and give it an informative name
- add new code or change code, and make a `Commit` for every change
    - you can select specific lines or chunks, you don't have to commit all changes at once
    - bundle related changes in a single commit and add a clear commit message. Spread unrelated changes over multiple commits.
- occasionally `Push` your changes to the repository on github (at least once a day, not too frequently as every push might trigger automated tests)

These steps are described into detail in a [separate workflow](https://inbo.github.io/git-course/workflow_rstudio.html) and in [this manual](https://inbo.github.io/git-course/course_rstudio.html#28_create_logical_commits).

# Create a pull request

Create a pull request when your work is ready to share with collaborators.

In RStudio, make sure all changes are committed and pushed.

In the GitHub repository:

- create a pull request by either
    - using the `Compare & pull request` button that appears after recent pushes
    - selecting your new feature branch and hitting the `New pull request` button
- make sure the correct branches are indicated:
    - 'base' mentions the branch where will merged to, often the master branch
    - the 'compare' branch is your feature branch
- adapt the title if needed, and describe what you did (you can scroll down to check your commits)
- hit `Create Pull request`
- request reviewers by adding them on the right top of the page

For an explanation including screenshots, see [here](https://inbo.github.io/git-course/course_rstudio.html#214_pull_requests) or [here](https://inbo.github.io/git-course/workflow_rstudio.html#edits_on_branch_are_ready).

__Remark:__ after creating a pull request, it is still possible to add new
commits to this branch and pull request.
After pushing new commits in RStudio, they appear in the pull request.
To show others that you are not finished yet, you can convert the pull request
to draft (right top of page, where you request reviewers)

# Revision of code

Reviewers will receive an email with a link to the pull request, and they can:

- inspect
    - __the changes__ on GitHub in the pull request by inspecting the tabs `Conversation`, `Commits` and `Files changed`
    - __the adapted version__ locally in RStudio after hitting `Pull` and select the branch name (mentioned at the top of the pull request in GitHub)
- review it on GitHub by following [this workflow](https://docs.github.com/en/github/collaborating-with-issues-and-pull-requests/reviewing-proposed-changes-in-a-pull-request#starting-a-review)
    - when reviewing, do not mix unrelated items in 1 proposed change, to allow the author to selectively accept changes
    - to propose major changes for a single issue yourself:
        - make a new branch in RStudio starting from the branch you are reviewing
        - add, commit and push your changes
        - make a pull request to merge your branch to the branch you are reviewing

During this revision, in the `Conversation` tab in the Pull request on GitHub:

- the author can accept suggestions of reviewers by choosing `Commit suggestions`
- suggestions or comments can be discussed using the comment boxes
- the author can re-request a reviewer after solving all comments

# Merge changes to master

Once you and your coworkers agreed on the final version in your branch, it can
be merged to the master branch:

- in RStudio, make sure to include novel changes in the master branch:
    - switch to the master branch
    - hit `Pull`
    - switch back to your feature branch
    - hit `More` and choose `Shell...`
    - type `git merge master` (or replace master by the name of the branch you want to merge to your branch)
    - you will be mentioned of any additions and/or conflicts
    - close the shell again
    - if conflicts have appeared,
        - solve them in your scripts
        - save the changes
        - commit all changes, make sure the solved conflicts are added
    - `Push` all new commits to GitHub
- on Github, below in the pull request:
    - hit `Merge pull request`
    - hit `Confirm merge`
    - and finally choose `Delete branch` to keep your repo clean and clear

For screenshots, see [here](https://inbo.github.io/git-course/workflow_rstudio.html#step_5:_code_review).

<div class="alert alert-danger">
When merging to the master branch or another important branch in the repo,
always do this on GitHub by using a pull request.
</div>

Once you are satisfied with a version, you can [create a release](https://docs.github.com/en/github/administering-a-repository/managing-releases-in-a-repository).
