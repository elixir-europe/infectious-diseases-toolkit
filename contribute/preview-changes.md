---
title: Preview changes
summary: Use your own fork to preview changes on the website.
---

## Introduction

This guide is mainly targeted at editors who have more rights than other contributors. Other contributors who want to preview their changes on their fork can skip towards the GitHub pages section right away.


## Make changes on your fork

As an editor with editing rights on the IDTk, changes made by clicking on the pencil icon will be committed to a branch on the actual IDTk itself. This is not a problem in normal circumstances, but when one wants to preview changes on one's own fork, this is not wanted.

### 1. Make sure you have forked the IDTk

Click on the 'fork' button in the right top corner to find out. If a fork is present under your personal GitHub ID, click on it. 

{% include image.html file="your_own_fork.png" alt="Your own fork" %}


Make sure you are in the `main` branch of your fork seen in the left top corner.

{% include image.html file="change_branch.png" alt="Change branch on GitHUb" %}


### 2. Make sure your fork is up to date

Click on the 'sync fork' button to make sure you have the latest changes of the IDTk in your fork. 'Update branch'.

{% include image.html file="sync_branch.png" alt="Click on the sync fork button." %}


### 3. Make changes

You can go to a folder and create a new file, or edit an existing file. See [Contributing using GitHub](/contribute/github-way) and [Creating a new page](/contribute/editorial-board-guide#create-a-new-page) for more information.

### 4. Commit to a new branch

This step is important. Make sure to commit to a new feature branch which you name in a logical way. 

{% include image.html file="commit_new_branch.png" alt="Propose changes on GitHub" %}


## Preview your changes using GitHub pages

Go to the Settings tab of your fork -> Pages -> Deploy from branch and select the newly created branch you made the change on. Save.
After a few minutes, you can find the preview at: <https://YOURGITHUBID.github.io/infectious-diseases-toolkit>

{% include image.html file="deploy_using_gh_pages.png" alt="Got to the settings tab in your repo to enable GitHub pages" %}


## Open a Pull Request (PR) with you changes

Got to your newly created branch and click 'Contribute'. This will create a PR to the IDTk.

{% include image.html file="create_pr_from_fork.png" alt="Create new PR from fork." %}

You can always make changes after the creation of this pull request by going to the files changed tab 

{% include image.html file="files_changed_github.png" alt="Files changed tab on GitHub" %}

and clicking on the 3 dots to edit the file again. Changes made this way will become visible in your preview automatically after a few minutes.

{% include image.html file="3_dots_github.png" alt="File change options on GitHub" %}
