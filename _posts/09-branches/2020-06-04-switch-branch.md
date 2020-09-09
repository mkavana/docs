---
layout: page
title: Switch branches in VSC
subtitle:
description: A guide to switching between branches in VSC
author: mkavana
date: 01 Jun 2020
post-number: 9.4
category: branches
position-in-category: 4
include-in-pre-reqs: "false"
include-in-quickstart: "false"
include-in-azdevops-quickstart: "false"
video_url: "none"
---

This guide describes how to switch from one Git branch to another branch using the Visual Studio Code (VSC) editor.

{% include prerequisites.html %}

## Topics in this guide

- [Switch between branches in VSC](#switch-branch)

{% include video.html %}

## Switch between branches in VSC {#switch-branch}

1. Open VSC and go to **File** > **Open Folder**.

    ![VSC window with file open folder dialogue highlighted.](../assets/images/09-branches/switch/switch-branch-001.png)

2. Go to the location on your computer where you cloned the GitHub/ AzDevOps repository (repo), and choose **Select Folder** (your local repo). The folder name for the local repo should be the same name as the project's GitHub/ AzDevOps repo, for example: **azfundedu**.

    ![VSC 'open folder' dialogue](../assets/images/09-branches/switch/switch-branch-002.png).

3. Select the VSC **Explorer** icon (left sidebar).

    Your local repo's folders and files should accessible be from the VSC **Explorer** pane (left side).

    ![Example repo folder structure in VSC explorer and VSC status bar](../assets/images/09-branches/switch/switch-branch-003.png)

4. The VSC **status bar**, at the bottom of the VSC editor, indicates which branch VSC is currently switched to. Select the branch name from the VSC status bar.

    For example, in the following image, the **master** branch is shown in the VSC status bar.

    ![VSC status bar](../assets/images/09-branches/switch/switch-branch-004.png)

    > **Note**: When you relaunch VSC, VSC opens on the last branch it was switched to when you closed VSC. This remains true until you explicitly switch VSC to a different branch.

5. When the VSC branch pane opens, note the list of available branches. Choose the branch you want, for example: **m5authkelly**.

    ![Example branch selected in the VSC branch pane](../assets/images/09-branches/switch/switch-branch-005.png)

6. VSC will switch to your chosen branch (as indicated in the VSC status bar). Any changes you make will be applied to the files on your chosen branch. To select another branch, repeat **Step 4 and 5**.

    ![Branch name in VSC status bar](../assets/images/09-branches/switch/switch-branch-006.png)

You've switched from one Git branch to another branch using VSC successfully.

{% include appendices.html %}

{% include paginator.html %}
