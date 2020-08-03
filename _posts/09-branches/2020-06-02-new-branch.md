---
layout: multi
title: Create new branch
subtitle: GitHub
description: A guide to creating a new branch in a GitHub repository using VSC
author: mkavana
date: 01 Jun 2020
post-number: 9.2
category: branches
position-in-category: 2
include-in-pre-reqs: "true"
include-in-quickstart: "true"
video_url: "none"
---

This guide describes using the Visual Studio Code (VSC) editor to create a new branch to work on.

Creating a new branch to work on allows you to view, create and edit markdown files and images without affecting the work of other contributors.

{% include prerequisites.html %}

## Topics in this guide

- [Create a new Git branch in VSC](#create-git-branch)
- [Branch naming conventions](#branch-name-convention)
- [Example branch names](#example-branch-names)

{% include video.html %}

## Create a new Git branch in VSC {#create-git-branch}

Complete the following steps to create a new Git branch using VSC.

1. Open **VSC** and go to **File** > **Open Folder**.

    ![VSC window with file 'open folder' dialogue](../assets/images/09-branches/create/github/git-createbranch-001.png)

2. Go to where you cloned the project's GitHub repository on your computer (your local repo). Choose **Select Folder**.

    The folder for your local repo should have the same name as the project's GitHub repo you cloned, for example: **azfundedu**.

    ![Open folder dialogue](../assets/images/09-branches/create/github/git-createbranch-002.png)

3. Your local repo's folder and file structure should be visible in the VSC explorer window. The VSC **status bar**, at the bottom of the editor, indicates the name of branch that VSC is currently switched to.

    In the following image, the **master** branch is shown in the VSC status bar. Switching VSC to a different branch is described in the guide [Switch branch]({{site.baseurl}}/branches/switch-branch.html).

    ![Example repo folder structure in VSC explorer window and VSC status bar](../assets/images/09-branches/create/github/git-createbranch-003.png)

    > **Note**: VSC opens in the same state it was in when you last closed it. Always check which branch, folders and files VSC is switched to. If you closed VSC previously using the `X` icon, without closing the folder in VSC, VSC may be switched to the wrong branch. You *must* ensure that VSC is switched to the correct branch to avoid inadvertently overwriting your files. The VSC **status bar**, at the bottom of the editor, indicates the name of branch that VSC is currently switched to.

4. Go to **View** > **Command Palette** and type **git branch**. From the resulting list of commands, choose `Git Create Branch From...`.

    ![List of Git commands available from the VSC Command Palette](../assets/images/09-branches/create/github/git-createbranch-004.png)

    > **Note**: There is another command called `Git Create Branch`. *Do not use this command*, doing so will base your new branch on whatever branch is listed in the VSC status bar. Select the correct command `Git Create Branch From...` instead.

5. In the subsequent pane, enter a name for the branch you are creating and then press **Enter**.

    The name of your new branch must conform to the branch naming convention described in [Branch naming conventions](#branch-name-convention).

    In the following image the example branch is named **m5techreviewkelly**.

    ![Example branch name typed into VSC Command Palette](../assets/images/09-branches/create/github/git-createbranch-005.png)

6. From the list of branches in the subsequent pane, select the branch that your new branch will be based on (i.e. set the **base branch** for your new branch).

    In the following image the branch **m5authekelly** is selected as the base branch.

    ![Example base branch selected from VSC Command Palette](../assets/images/09-branches/create/github/git-createbranch-006.png)

    > **Note**: If you are *not* prompted to choose a base branch, you may have selected the wrong command `Git Create Branch`. Return to **Step 4** and select the correct command `Git Create Branch From...` instead.

7. Your new branch should open in VSC. The VSC status bar will indicate that VSC has switched to the new branch you created.

    ![VSC switched to new branch indicated in VSC status bar](../assets/images/09-branches/create/github/git-createbranch-007.png)

    > **Note**: Your new branch is not on GitHub yet. Only *you* can access and see your new (local) branch, until you send your new branch to GitHub. Send (or **push**) your new branch to GitHub using the instructions provided in the guide [Upload (push) your changes]({{site.baseurl}}/branches/push-branch.html). Pushing your branch to GitHub will ensure that your new branch is present on GitHub, backed up, and visible to other GitHub contributors.

You have created a new branch using VSC successfully.

## Branch naming conventions {#branch-name-convention}

Generally, each contributor (author, reviewer, etc.) must work in their own branch. A separate branch for each module is also required. This approach keeps the content separated per contributor, at each stage in the process, and on a module by module basis.

A new branch is usually created from the master branch of the project's GitHub repo. When you create a new branch, your branch name should describe your branch's content and make the branch's purpose and owner clear to other contributors.

Use the following branch naming convention (all lower case) to name your new branch:

`m <module number> <task> <contributor's surname>`:

- The prefix `m` is for “module”.
- `<module number>` refers to the module number that the file you are working on belongs to.
- `<task>` is a short code for the stage in the process the file is at. The task short codes are listed in the next section.
- Add your `<surname>` as a suffix to distinguish your work from the work of other contributors.

Examples of branch names are provided in [Example branch names](#example-branch-names).

### Task short codes

Use the following task short codes in your branch name to indicate the stage in the process that the file you are working on is at.

|Role|Process stage|Task short code|
|---|---|---|
|*Author*|Content authoring|`auth`|
|*Reviewer*|Instructional design review|`idreview`|
|*Reviewer*|Technical review|`techreview`|
|*Reviewer*|Academic review|`acadreview`|
|*Editor*|Copy editing|`copyedit`|
|*Prepublication stylist*|Prepublication styling and formatting|`prepub`|

## Example branch names {#example-branch-names}

The following are examples of branch names that conform to the branch naming convention, with descriptions of how the branch names are constructed.

### Example authoring branch name

The following explains how the example authoring branch name `m6authlee` is constructed.

- `m` is an abbreviation for "module".
- `6` is the number of the module that the file belongs to.
- `auth` is a short code for "content authoring".
- `lee` is a reference to the author's surname.

Putting the previous items together results in the authoring branch name `m6authlee`.

### Example CE reviewer's branch name

The following explains how the example reviewer branch name `m6-cereview-lee` is constructed.

- `m` is an abbreviation for "module".
- `6` is the number of the module that the file(s) for review belong(s) to.
- `cereview` is a short code for "content editing review".
- `lee` is a reference to the reviewer's surname.

Putting the previous items together results in the reviewer branch name `m6-cereview-lee`.

{% include appendices.html %}

{% include paginator.html %}
