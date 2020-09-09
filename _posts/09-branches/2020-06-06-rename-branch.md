---
layout: page
title: Rename branch
subtitle:
description: A guide to renaming a Git branch using VSC.
author: mkavana
date: 01 Jun 2020
post-number: 9.6
category: branches
position-in-category: 6
include-in-pre-reqs: "false"
include-in-quickstart: "false"
include-in-azdevops-quickstart: "false"
video_url: "none"
---

This guide describes how to rename a Git branch using the Visual Studio Code (VSC) editor.

> **Note**: Take care when renaming a branch, and *only rename a branch if you're sure you need to*.
>

{% include prerequisites.html %}

## Topics in this guide

- [Rename a Git branch using VSC](#rename-branch)

{% include video.html %}

## Rename a Git branch using VSC {#rename-branch}

1. Open VSC, and choose **File** > **Open folder** (top menu).

    !['Open folder' top menu option in VSC](../assets/images/09-branches/rename/rename-001.png)

2. Use the **VSC open folder explorer** to select the local repo folder on your computer, then choose **Select folder**.

    !['Select folder' option in the 'VSC open folder explorer'](../assets/images/09-branches/rename/rename-002.png)

3. From the VSC top menu, choose **Terminal** > **New Terminal**.

    !['New Terminal' top menu option in VSC](../assets/images/09-branches/rename/rename-003.png)

    > **Note**: The **VSC status bar**, at the bottom of the editor window, indicates the name of the branch that VSC is currently switched to. In the previous image, the **VSC status bar** indicates that VSC is currently switched to the branch called **old-name**. The branch name in the **VSC status bar** will change to the new branch name after you've renamed the branch.
    >

4. In the **VSC Terminal**, type the following command to rename your local branch, then press **Enter**.

    For example, in the following sample command and image, the branch is renamed from **old-name** to **new-name**. Replace **old-name** and **new-name** with whatever branch names you require.

    ```bash
    git branch -m old-name new-name
    ```

    !['Git branch rename' command in the 'VSC Terminal'](../assets/images/09-branches/rename/rename-004a.png)

    The branch name in the **VSC status bar** should now change to the new branch name.

    ![The new branch name in the 'VSC status bar'](../assets/images/09-branches/rename/rename-004b.png)

    > **Note**: The Git branch command option `-m` is short for **move**, and the `-m` command option is also used to rename a Git branch. Information about the Git move (rename) branch command, and other options, is available from the [Software Freedom Conservancy's Git branch documentation](https://git-scm.com/docs/git-branch).
    >

5. Delete the old branch name from GitHub/ AzDevOps by typing the following command into the **VSC Terminal**, and then press **Enter**:

    ```bash
    git push origin --delete old-name
    ```

    !['Git delete branch' command in the 'VSC Terminal'](../assets/images/09-branches/rename/rename-005a.png)

    A message in the **VSC Terminal** confirms that the branch is deleted from GitHub/ AzDevOps.

    !['Git delete branch' confirmation message the 'VSC Terminal'](../assets/images/09-branches/rename/rename-005b.png)

6. Push (send) the new branch name to GitHub/ AzDevOps by typing the following command into the **VSC Terminal**, and then press **Enter**.

    ```bash
    git push origin new-name
    ```

    !['Git push new branch name' command in the 'VSC Terminal'](../assets/images/09-branches/rename/rename-006a.png)

    A message in the **VSC Terminal** confirms that the branch is renamed on GitHub/ AzDevOps.

    !['Git push new branch name' confirmation message the 'VSC Terminal'](../assets/images/09-branches/rename/rename-006b.png)

7. Reset the link between your renamed local branch and the new (upstream) branch you pushed to GitHub/ AzDevOps by typing the following command into the **VSC Terminal**, and then press **Enter**.

    ```bash
    git push origin -u new-name
    ```

    !['Git set upstream command' in the 'VSC Terminal'](../assets/images/09-branches/rename/rename-007a.png)

    The **Everything up-to-date** message in the **VSC Terminal** confirms that the branch link is reset.

    !['Everything up-to-date' confirmation message the 'VSC Terminal'](../assets/images/09-branches/rename/rename-007b.png)

8. The **VSC status bar** should indicate that VSC is currently switched to your renamed branch. You can now make, save, stage, commit, and push file changes between the renamed local branch and GitHub/ AzDevOps.

    ![Current branch set to new branch name in the 'VSC status bar'](../assets/images/09-branches/rename/rename-008.png)

You've renamed a branch using VSC successfully.

{% include appendices.html %}

{% include paginator.html %}
