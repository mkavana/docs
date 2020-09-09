---
layout: page
title: Update branch (pull) in VSC
subtitle: Pull latest files
description: A guide to updating a local repo with the latest files from a remote repo using the Git pull command
author: mkavana
date: 01 Jun 2020
post-number: 9.3
category: branches
position-in-category: 3
include-in-pre-reqs: "false"
include-in-quickstart: "false"
include-in-azdevops-quickstart: "false"
video_url: "none"
---

This guide describes using the Visual Studio Code (VSC) editor to get (or **pull**) the latest files from GitHub/ AzDevOps.

{% include prerequisites.html %}

## Topics in this guide

- [Overview of the Git pull command](#overview-git-pull)
- [Get the latest files from GitHub/ AzDevOps with VSC](#steps=git-pull)

{% include video.html %}

## Overview of the Git pull command {#overview-git-pull}

Git branching makes it possible for multiple contributors to edit the same files in a GitHub/ AzDevOps repository (remote repo). Other contributors might update the files in a remote repo at any time, so it's important to keep the files in your local repo up to date with the remote repo.

Update your local repo when you begin your working day, throughout the day, and whenever you need a file or feature from the remote repo that you don't have locally. Keeping your local repo up to date helps to avoid "merge conflicts", which arise from attempts to merge incompatible versions of the same file.

### Git pull

The `git pull` command gets information about the latest files from the remote repo and merges the files from the remote repo with the files in your local repo. The `git pull` command can retrieve and send files to and from different branches.

> **Note**: Whenever you pull files into a specific branch, you *must* ensure that VSC is switched to the correct branch to avoid inadvertently overwriting files. The VSC **status bar**, at the bottom of the editor, indicates the name of branch that VSC is currently switched to.
>

Save any changes you make to your local repo regularly (using Git **stage** and **commit**). For details about Git terminology and file saving actions visit the guides [Terminology and concepts]({{site.baseurl}}/workflow/terminology.html) and [send (push) files]({{site.baseurl}}/branches/push-files.html).

## Get the latest files from GitHub/ AzDevOps with VSC {#steps-git-pull}

Complete the following steps to get the latest files from GitHub/ AzDevOps into your local repo using `git pull` in VSC.

1. In VSC, open your local repo (**File** > **Open Folder**), and select the VSC **Explorer** icon (left sidebar).

    ![Local repo folder with VSC Explorer icon selected from the left sidebar](../assets/images/09-branches/pull/git-pull-001.png)

2. Switch VSC to the branch you want to update.

    The VSC **status bar**, at the bottom of the editor, indicates the name of branch that VSC is currently switched to.

    For example, in the following image, the VSC **status bar** indicates that VSC is currently switched to the **master** branch. Switching VSC to a different branch is described in the guide [Switch branch]({{site.baseurl}}/branches/switch-branch.html). The local repo's folders and files are accessible from the VSC Explorer pane (on the left side).

    ![Local repo folder structure and status bar in VSC](../assets/images/09-branches/pull/git-pull-002.png)

3. Go to **Terminal** > **New Terminal**.

    ![Terminal menu tab and new terminal option in VSC](../assets/images/09-branches/pull/git-pull-003.png)

4. Type **git pull** into the resulting terminal window, select **git pull**, and press **Enter**.

    ![Git pull command running in a VSC terminal](../assets/images/09-branches/pull/git-pull-004.png)

    The command `git pull` will commence retrieving files from GitHub/ AzDevOps. The spinning arrows in the status bar, beside the branch name, indicate the progress of the pull command.

    > **Note**: You *must* always use the **VSC Terminal** to perform `git pull` actions. Running the `git pull` command from the **VSC Command Palette** will not always update the files in your local repo correctly.
    >

5. When a message indicating that the `git pull` command has completed appears in the VSC terminal, close the terminal window using the `X` (upper right side corner of the terminal window).

    ![Git pull completed message in VSC terminal](../assets/images/09-branches/pull/git-pull-005.png)

    > **Note**: If there are changes pending in your local branch, and you run the Git pull command, you may receive the message *cannot overwrite existing changes*. To pull the latest files from GitHub/ AzDevOps successfully, save the changes first then run the Git pull command again.
    >

{% include appendices.html %}

{% include paginator.html %}
