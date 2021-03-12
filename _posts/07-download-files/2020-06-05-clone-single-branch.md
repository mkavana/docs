---
layout: page
title: Clone single folder
subtitle: GitHub
description: A guide to cloning a single folder from a specific branch
author: mkavana
date: 01 Jun 2020
post-number: 7.5
category: download-files
position-in-category: 5
include-in-pre-reqs: "false"
include-in-quickstart: "false"
include-in-azdevops-quickstart: "false"
video_url: "none"
---

This guide describes how to clone a single folder (directory) and specific branch from a GitHub repository (repo).

{% include prerequisites.html %}

## Topics in this guide

- [Clone a single folder and branch from GitHub](#single-folder)

{% include video.html %}

## Clone a single folder and branch from GitHub {#single-folder}

1. Open a web browser, then go to github.com, and sign in.

1. Go to the GitHub page for the author's fork/ repo you want to clone.

    For example, go to **https://github.com/username/example-repo**.

1. Select the **Code** dropdown, then copy the clone URL to your clipboard.

    For example, copy the URL **https://github.com/username/example-repo.git** to your clipboard.

1. On your computer, open the Git Bash application.

1. In Git Bash, change into the directory where you want to clone the author's fork/ repo.

    For example, to change into the directory **myGitDirectory** on the path **C:/**, enter the following command.

    ```Bash
    cd C:/myGitDirectory
    ```

1. Create an "empty" repo on your computer by cloning a single branch from the author's fork/ repo, and paste in the clone URL you copied previously.

    In the following example, the single branch is named **example-branch-name** and the clone URL for author's fork/ repo is **https://github.com/username/example-repo.git**. Replace the example branch name and the clone URL with the branch and fork/ repo you want to clone.

    ```Bash
    git clone --filter=blob:none --sparse https://github.com/username/example-repo.git ---branch example-branch-name --single-branch
    ```

1. Change into the directory containing the repo you cloned.

    ```Bash
    cd example-repo
    ```

1. Initialize the repo with the `sparse-checkout` command.

    ```Bash
    git sparse-checkout init --cone
    ```

1. Checkout the specific sub-directory you require.

   For example, to checkout a sub-directory named **my/sub/directory**, use the following command.

    ```Bash
    git sparse-checkout add my/sub/directory
    ```

1. Open the Visual Studio Code editor (VSC).

1. In VSC, from the top left menu bar, select **File** > **Open Folder**.

1. Navigate to the where you cloned the author's fork/ repo on your computer, select the sub-directory containing the files you want to access, and then choose **Select Folder**.

    For example, navigate to the directory **c:\myGitDirectory** and select the sub-directory **example-repo**.

    > **Note**: In the bottom left of VSC status bar confirm that VSC is switched to the correct branch.
    >

1. Use the **EXPLORER** pane to locate the directories and files you need.

    For example, locate the the files in the directory **example-repo/my/sub/directory**.

1. Edit the file(s), then save, stage, commit and push your file changes to GitHub.

{% include appendices.html %}

{% include paginator.html %}