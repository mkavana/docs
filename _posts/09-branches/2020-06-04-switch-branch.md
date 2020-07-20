---
layout: multi
title: Switch branches
subtitle: GitHub
description: A guide to switching between branches in VSC
author: mkavana
date: 01 Jun 2020
post-number: 9.4
category: branches
position-in-category: 4
include-in-pre-reqs: "false"
include-in-quickstart: "false"
video_url: "none"
---

This guide describes how to switch from one Git branch to another branch using the Visual Studio Code (VSC) editor.

{% include prerequisites.html %}

## Topics in this guide

- [Topic 1: Switch between branches in VSC](#topic1)

{% include video.html %}

## Topic 1: Switch between branches in VSC {#topic1}

1. Open VSC and go to **File** > **Open Folder**.

    ![VSC window with file open folder dialogue highlighted.](../assets/images/09-branches/switch/github/switch-branch-001.png)

2. Go to the location on your computer where you cloned the GitHub repository, and choose **Select Folder** (your local repo). The folder name for the local repo should be the same name as the project's GitHub repo, for example: **azfundedu**.

    ![VSC 'open folder' dialogue](../assets/images/09-branches/switch/github/switch-branch-002.png).

3. The local repo folder and file structure should be visible in the VSC **Explorer** window (side bar). The VSC **status bar**, at the bottom of the VSC editor, indicates which branch VSC is currently switched to. Select the branch name from the VSC status bar.

    In the following image, the **master** branch is shown in the VSC status bar.

    ![Example repo folder structure in VSC explorer and VSC status bar](../assets/images/09-branches/switch/github/switch-branch-003.png)

    > **Note**: When you relaunch VSC, VSC opens on the last branch it was switched to when you closed VSC. This remains true until you explicitly switch VSC to a different branch.

4. When the VSC branch pane opens, note the list of available branches. Choose the branch you want, for example: **m5authkelly**.

    ![Example branch selected in the VSC branch pane](../assets/images/09-branches/switch/github/switch-branch-004.png)

5. VSC will switch to your chosen branch (as indicated in the VSC status bar). Any changes you make will be applied to the files on your chosen branch. To select another branch, repeat **Step 1 to 4**.

    ![Branch name in VSC status bar](../assets/images/09-branches/switch/github/switch-branch-005.png)

{% include appendices.html %}

{% include paginator.html %}
