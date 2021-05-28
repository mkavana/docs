---
layout: page
title: Fetch upstream changes
subtitle: GitHub
description: A guide to updating a local repo with changes from an upstream GitHub repo.
author: mkavana
date: 01 Jun 2020
post-number: 7.6
category: download-files
position-in-category: 6
include-in-pre-reqs: "false"
include-in-quickstart: "false"
include-in-azdevops-quickstart: "false"
video_url: "none"
---

This guide describes how to fetch file changes from an upstream GitHub repository (repo), merge them into a GitHub fork, and pull the file changes from the GitHub fork into a local clone.

## Prerequisites

- To follow this guide, you should be familiar with using Git, GitHub and Visual Studio Code (VSC).

## Topics in this guide

- [Fetch and merge files changes from upstream](#fetch-upstream)
- [Pull file changes from a GitHub fork into a local clone](#pull-changes-locally)

{% include video.html %}

## Fetch and merge files changes from upstream {#fetch-upstream}

This topic describes how to fetch file changes from the master branch of an upstream repo (Microsoft Docs), and merge these file changes into the master branch of a fork on GitHub.

1. Sign in at [GitHub.com](https://github.com).

    > **Note**: If prompted, on your GitHub landing page, follow the **Single sign-on** link, and then authenticate with your 'v dash' user account credentials.
    >

1. Go to the URL for your GitHub fork (*YourFork*).

    For example, go to the URL `https://github.com/< your-GitHub-username >/learn-pr`.

1. On your GitHub fork\'s landing page, set the branch to **master**.

1. Select **Fetch upstream**.

    > **Note**: Review the available options.
    >
    > - *Compare*. Examine the similarities and differences between the files in *MicrosoftDocs:master* and the files in *YourFork:master*.
    > - *Fetch and merge*. Retrieve (fetch) all file changes from *MicrosoftDocs:master* that are not present in *YourFork:master*, and combine (merge) these file changes into *YourFork:master*.
    >

1. Choose **Fetch and merge**.

    In the following image, the example GitHub fork *mkavana:learn-pr* is set to the **master** branch. **Fetch upstream** is selected, and the options to **Compare** or **Fetch and merge** are available.

    ![Example GitHub fork set to the master branch. Fetch upstream is selected, and options to Compare or Fetch and merge are available](../assets/images/07-download-files/fetch-upstream/github/upstream-01-05.png)

## Pull file changes from a GitHub fork into a local clone {#pull-changes-locally}

This topic describes using VSC to pull file changes from the master branch of a GitHub fork into a local clone (on your computer).

1. Open VSC.

1. Open your local clone by using **File** \> **Open folder** \> **Select folder** (top menu).

1. Switch VSC to the **master** by branch using the **branch selector** icon (bottom left).

1. Select the **Source Control** icon (left side menu).

1. Choose the **View and More Actions** ellipses (`...`) icon.

1. From the **View and More Actions** menu, select **Pull, Push** \> **Pull from…**.

    The following image demonstrates the VSC user selections: **Source Control** \> **View and More Actions** \> **Pull, Push** \> **Pull from…**.

    ![VSC user selections: Source Control, View and More Actions, Pull, Push, and Pull from…](../assets/images/07-download-files/fetch-upstream/github/upstream-02-06.png)

1. Choose the URL for *your* GitHub fork from the prompt to **Pick a remote to pull the branch from…**.

    For example, in the following image, the chosen GitHub fork URL is `origin https://github.com/mkavana/learn-pr`.

    ![Example GitHub fork URL](../assets/images/07-download-files/fetch-upstream/github/upstream-02-07.png)

1. Select **origin/master** from the prompt to **Pick a branch to pull from**.

    For example, in the following image the selected branch is **origin/master**.

    ![Example selected branch origin/master](../assets/images/07-download-files/fetch-upstream/github/upstream-02-08.png)

Congratulations\! You've fetched upstream file changes from *MicrosoftDocs:master*, merged them into the GitHub fork *YourFork:master*, and pulled the file changes from *YourFork:master* into a local clone.

{% include appendices.html %}

{% include paginator.html %}
