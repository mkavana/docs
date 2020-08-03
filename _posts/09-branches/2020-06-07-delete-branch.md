---
layout: page
title: Delete branch
subtitle:
description: A guide to deleting a Git branch using VSC and GitHub
author: mkavana
date: 01 Jun 2020
post-number: 9.7
category: branches
position-in-category: 7
include-in-pre-reqs: "false"
include-in-quickstart: "false"
video_url: "none"
---

This guide describes how to delete a Git branch using the Visual Studio Code (VSC) editor and GitHub.

> **Note**: Take care when deleting a branch, and only delete a branch if you are sure that you need to.
>
> The options for deleting a Git branch described in this guide only work on branches that have been pushed to, and merged with, GitHub already. Forcing the deletion of unmerged branches is beyond the scope of this guide.
>
> Information about the Git `delete branch` command is available from the [Software Freedom Conservancy's Git branch documentation](https://git-scm.com/docs/git-branch).
>

{% include prerequisites.html %}

## Topics in this guide

- [Delete a branch using VSC](#vsc-delete-branch)
- [Delete a branch using GitHub](#github-delete-branch)

{% include video.html %}

## Delete a branch using VSC {#vsc-delete-branch}

Complete the following steps to delete a Git branch using VSC.

> **Note**: To complete this guide you *must* know how to switch branches, as described in the guide [Switch branches]({{site.baseurl}}//branches/switch-branch.html).

1. Open VSC, and from the top menu choose **File** > **Open folder**.

    !['Open folder' top menu option in VSC](../assets/images/09-branches/delete/del-branch-vsc-001.png)

2. Use the **VSC open folder explorer** to select the local repository folder (repo) on your computer, then choose **Select folder**.

    !['Select folder' option in the 'VSC open folder explorer'](../assets/images/09-branches/delete/del-branch-vsc-002.png)

3. From the VSC top menu, choose **Terminal** > **New Terminal**.

    !['New Terminal' top menu option in VSC](../assets/images/09-branches/delete/del-branch-vsc-003.png)

    > **Note**: The **VSC status bar**, at the bottom of the editor window, indicates the name of the branch that VSC is currently switched to. For example, in the previous image, the **VSC status bar** indicates that VSC is currently switched to the branch called **master**.
    >
    > You can't delete the branch that VSC (or Git) is currently switched to. Switch to a branch *other than the branch you want to delete*, and then continue following this guide.
    >

4. In the **VSC Terminal**, type the following command to delete the branch from your local repo, and then press **Enter**.

    For example, in the following image, the local branch **old-branch** will be deleted. Replace **branch_name** with the name of the local branch you want to delete.

    ```bash
    git branch --delete <branch_name>
    ```

    !['Git delete branch' command in the 'VSC Terminal'](../assets/images/09-branches/delete/del-branch-vsc-004a.png)

    A message in the **VSC Terminal** confirms that the branch is deleted from your local repo.

    !['Git delete local branch' confirmation message the 'VSC Terminal'](../assets/images/09-branches/delete/del-branch-vsc-004b.png)

5. Delete the branch from GitHub with the `git push` command by typing the following command into the **VSC Terminal**, and then press **Enter**.

    ```bash
    git push origin --delete <branch_name>
    ```

    For example, in the following image, the GitHub branch **old-branch** will be deleted from GitHub. Replace **branch_name** with the name of the GitHub branch you want to delete.

    !['Git push delete branch' command in the 'VSC Terminal'](../assets/images/09-branches/delete/del-branch-vsc-005a.png)

    A message in the **VSC Terminal** confirms that the branch is deleted from GitHub.

    !['Git push delete remote branch' confirmation message the 'VSC Terminal'](../assets/images/09-branches/delete/del-branch-vsc-005b.png)

You have deleted a Git branch using VSC successfully.

## Delete a branch using GitHub {#github-delete-branch}

Complete the following steps to delete a Git branch using GitHub.

> **Note**: Deleting a branch using GitHub removes the branch from GitHub only. Your local repo might retain a copy of the branch until you pull updates from GitHub into your local repo, or clone the GitHub repo again. To delete a branch from your local repo and from GitHub, follow the steps in [Delete a branch using VSC](#vsc-delete-branch).

1. Open a web browser, go to the URL for the project's GitHub repo, and sign in to GitHub.

2. Select the **Branches** icon.

    ![Branches icon on GitHub](../assets/images/09-branches/delete/del-branch-github-002.png)

3. Select the **trash can** icon beside the branch you want delete (on the right side).

    For example, in the following image, the branch called **old-branch** will be deleted.

    ![Trash icon for deleting a branch from GitHub](../assets/images/09-branches/delete/del-branch-github-003.png)

4. The **Deleted just now** message and **Restore** button beside the branch name indicate that the branch has been deleted from GitHub.

    !['Deleted just now' message and 'Restore' button beside the deleted branch on GitHub](../assets/images/09-branches/delete/del-branch-github-004.png)

You have deleted a Git branch using GitHub successfully.

{% include appendices.html %}

{% include paginator.html %}
