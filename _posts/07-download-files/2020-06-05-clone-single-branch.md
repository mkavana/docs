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

This guide describes how to clone a single folder (directory) on a specific branch from a GitHub repository (repo).

{% include prerequisites.html %}

## Topics in this guide

- [Clone a single folder and branch from GitHub](#single-folder)

{% include video.html %}

## Clone a single folder and branch from GitHub {#single-folder}

1. Gather the following details for the GitHub repo (or fork) that contains the files you want to clone.

    - URL of the GitHub fork/ repo; for example, `https://github.com/mkavana/repo-example`
    - Name of the branch that the required files are on; for example, `Mod02-branch`
    - Path to the (sub) directory that contains the required files; for example, `Mod02-example-directory/sub-directory/`

1. Open a web browser, then go to [github.com](https://github.com), and sign in.

1. Go to the URL of the GitHub fork/ repo you want to clone.

    For example, go to `https://github.com/mkavana/repo-example`.

1. Select the **Code** dropdown, then copy the clone URL to your clipboard.

    For example, copy the URL *`https://github.com/mkavana/repo-example.git` to your clipboard.

    ![alt text](../assets/images/07-download-files/single-dir/github/single-dir-004.png)

1. On your computer, open the Visual Studio Code editor (VSC).

1. In VSC, from the top menu, select **Terminal** > **New Terminal** or use the shortcut keys **CTRL** + **SHIFT** + **'**.

    ![alt text](../assets/images/07-download-files/single-dir/github/single-dir-006.png)

1. In the VSC **TERMINAL** window, change into the directory where you want to clone the fork/ repo.

    For example, to change into the directory **myGitDirectory** on the path **C:/**, enter the following command into the VSC terminal.

    ```sh
    cd C:/myGitDirectory
    ```

    ![alt text](../assets/images/07-download-files/single-dir/github/single-dir-007.png)

1. Create an "empty" repo on your computer by cloning a single branch from GitHub, and by pasting the clone URL you copied previously.

    > **Note**: In the following example, the single branch is named **Mod02-branch** and the clone URL for the fork/ repo is `https://github.com/mkavana/repo-example.git`. Replace the example branch name and the clone URL with the branch and fork/ repo you want to clone.
    >

    Enter the following command into the VSC terminal.

    ```sh
    git clone --filter=blob:none --sparse https://github.com/mkavana/repo-example.git ---branch Mod02-branch --single-branch
    ```

    ![alt text](../assets/images/07-download-files/single-dir/github/single-dir-008.png)

1. After cloning is complete, change into the directory containing the repo you cloned.

    Enter the following command into the VSC terminal.

    ```sh
    cd repo-example
    ```

1. Initialize the repo with the `sparse-checkout` command.

    Enter the following command into the VSC terminal.

    ```sh
    git sparse-checkout init --cone
    ```

    ![alt text](../assets/images/07-download-files/single-dir/github/single-dir-010.png)

1. Checkout the specific sub-directory you require.

    For example, to checkout a sub-directory named **Mod02-example-directory/sub-directory/**, enter the following command into the VSC terminal.

    ```sh
    git sparse-checkout add Mod02-example-directory/sub-directory/
    ```

    ![alt text](../assets/images/07-download-files/single-dir/github/single-dir-011.png)

1. Close the VSC terminal panel by using the **X** icon (top right side of the panel).

    ![alt text](../assets/images/07-download-files/single-dir/github/single-dir-012.png)

1. In VSC, from the top left menu bar, select **File** > **Open Folder**.

    ![alt text](../assets/images/07-download-files/single-dir/github/single-dir-013.png)

1. In the VSC **Open folder** pane, navigate to the where you cloned the fork/ repo on your computer, select the repo directory, and then choose **Select Folder**.

    For example, navigate to the directory **c:\myGitDirectory**, and select the repo directory **repo-example**.

    ![alt text](../assets/images/07-download-files/single-dir/github/single-dir-014.png)

1. Confirm that VSC is switched to the correct branch.

    > **Note**: In VSC, the current branch is indicated in the status bar in the bottom left.

    In the following image, the current branch is named **Mod02-branch**.

    ![alt text](../assets/images/07-download-files/single-dir/github/single-dir-015.png)

1. Use the VSC **EXPLORER** pane to locate and open the sub-directories and files you need to edit.

    For example, locate the the file name **01-nested-file \.md** on the path **repo-example-repo/Mod02-example-directory/sub-directory/**.

    ![alt text](../assets/images/07-download-files/single-dir/github/single-dir-016.png)

1. Edit the file(s), then save, stage, commit, and push your file changes to GitHub.

{% include appendices.html %}

{% include paginator.html %}
