---
layout: multi
title: Update branch
subtitle: GitHub - pull latest files from GitHub
description: A guide to updating a local repo with the latest files from a GitHub repo using the Git pull command
author: mkavana
date: 01 Jun 2020
post-number: 9.3
category: branches
position-in-category: 3
include-in-pre-reqs: "false"
include-in-quickstart: "false"
video_url: "none"
---

This guide describes how to get (or **pull**) the latest files from GitHub using the Visual Studio Code (VSC) editor.

{% include prerequisites.html %}

## Topics in this guide

- [Topic 1: Overview of the Git pull command](#topic1)
- [Topic 2: Get the latest version of the GitHub repo](#topic2)

{% include video.html %}

## Topic 1: Overview of the Git pull command {#topic1}

Git branching makes it possible for multiple contributors to edit the same files in a GitHub repo. Other contributors may update files on GitHub at any time, so it's important to keep the files in your local repo up to date with GitHub.

Update your local repo when you begin your working day, throughout the day, and whenever you need a file or feature from GitHub that you don't have locally. Keeping your local repo up to date helps to avoid "merge conflicts", which arise from attempts to merge incompatible versions of the same file.

### Git pull

The `git pull` command gets information about the latest files from GitHub and merges the files from GitHub with the files in your local repo. The `git pull` command can retrieve and send files to and from different branches.

> **Note**: Whenever you pull files into a specific branch, you *must* ensure that VSC is switched to the correct branch to avoid inadvertently overwriting files. The VSC **status bar**, at the bottom of the editor, indicates the name of branch that VSC is currently switched to.
>

Save any changes you make to your local repo regularly (using Git **stage** and **commit**). For details about Git terminology and file saving actions visit the guides [Terminology and concepts]({{ site.baseurl }}/workflow/terminology.html) and [send (push) files]({{ site.baseurl }}/branches/push-branch.html).

## Topic 2: Get the latest version of the GitHub rep {#topic2}

Complete the following steps to get the latest files from GitHub into your local repo using `git pull` in VSC.

1. In VSC, open your local repo (**File** > **Open Folder**).

2. Switch VSC to the branch you want to update.

    The VSC **status bar**, at the bottom of the editor, indicates the name of branch that VSC is currently switched to.

    For example, in the following image, the VSC **status bar** indicates that VSC is currently switched to the **master** branch.

    ![Local repo folder structure and status bar in VSC](../assets/images/09-branches/pull/github/git-pull-002.png)

3. Go to **Terminal** > **New Terminal**.

    ![Terminal menu tab and new terminal option in VSC](../assets/images/09-branches/pull/github/git-pull-003.png)

4. Type **git pull** into the resulting terminal window, select **git pull**, and press **Enter**.

    ![Git pull command running in a VSC terminal](../assets/images/09-branches/pull/github/git-pull-004.png)

    The command `git pull` will commence retrieving files from GitHub. The spinning arrows in the status bar, beside the branch name, indicate the progress of the pull command.

    > **Note**: You *must* always use the **VSC Terminal** to perform `git pull` actions. Running the `git pull` command from the **VSC Command Palette** will not always update the files in your local repo correctly.

5. When a message indicating that the `git pull` command has completed appears in the VSC terminal, close the terminal window using the `X` (upper right side corner of the terminal window).

    ![Git pull completed message in VSC terminal](../assets/images/09-branches/pull/github/git-pull-005.png)

    > **Note**: If there are changes pending in your local branch, and you run the Git pull command, you may receive the message *cannot overwrite existing changes*. To pull the latest files from GitHub successfully, save the changes first then run the Git pull command again.

{% include appendices.html %}

{% include paginator.html %}
