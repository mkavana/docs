---
layout: multi
title: Delete branch
subtitle: AzDevOps
description: A guide to deleting a Git branch using VSC and AzDevOps.
author: mkavana
date: 01 Jun 2020
post-number: 9.7
#category: branches
#position-in-category: 7
include-in-pre-reqs: "false"
include-in-quickstart: "false"
video_url: "none"
---

This guide describes how to delete a branch using the Visual Studio Code (VSC) editor and AzDevOps.

> **Note**: Take care when deleting a branch, and *only delete a branch if you're sure that you need to*.
>
> The options for deleting a branch described in this guide only work on branches that have been pushed to, and merged with, AzDevOps already. Forcing the deletion of unmerged branches is beyond the scope of this guide.
>
> Information about the Git `delete branch` command is available from the [Software Freedom Conservancy's Git branch documentation](https://git-scm.com/docs/git-branch).
>

{% include prerequisites.html %}

## Topics in this guide

- [Delete a branch using VSC](#azdev-vsc-delete-branch)
- [Delete a branch using AzDevOps](#azdev-delete-branch)

{% include video.html %}

## Delete a branch using VSC {#azdev-vsc-delete-branch}

Complete the following steps to delete a branch using VSC.

> **Note**: To complete this guide you *must* know how to switch branches, as described in the guide [Switch branches]({{site.baseurl}}/branches/switch-branch.html).
>

1. Open VSC, and choose **File** > **Open folder** from the top menu.

    !['Open folder' top menu option in VSC](../assets/images/09-branches/delete/azdev/del-branch-vsc-001.png)

2. Use the **VSC open folder explorer** to select the local repository folder (repo) on your computer, and then choose **Select folder**.

    !['Select folder' option in the 'VSC open folder explorer'](../assets/images/09-branches/delete/azdev/del-branch-vsc-002.png)

3. From the VSC top menu, choose **Terminal** > **New Terminal**.

    !['New Terminal' top menu option in VSC](../assets/images/09-branches/delete/azdev/del-branch-vsc-003.png)

    > **Note**: The **VSC status bar**, at the bottom of the editor window, indicates the name of the branch that VSC is currently switched to. For example, in the previous image, the **VSC status bar** indicates that VSC is currently switched to the branch named **master**.
    >
    > You can't delete the branch that VSC (or Git) is currently switched to. Switch to a branch *other than the branch you want to delete*, and then continue following this guide.
    >

4. In the **VSC Terminal**, type the following command to delete the branch from your local repo, and then press **Enter**.

    For example, in the following image, the local branch **old-branch** will be deleted. Replace **branch_name** with the name of the local branch you want to delete.

    ```bash
    git branch --delete <branch_name>
    ```

    !['Git delete branch' command in the 'VSC Terminal'](../assets/images/09-branches/delete/azdev/del-branch-vsc-004a.png)

    A message in the **VSC Terminal** confirms that the branch is deleted from your local repo.

    !['Git delete local branch' confirmation message the 'VSC Terminal'](../assets/images/09-branches/delete/azdev/del-branch-vsc-004b.png)

5. Delete the branch from AzDevOps with the `git push` command by typing the following command into the **VSC Terminal**, and then press **Enter**.

    ```bash
    git push origin --delete <branch_name>
    ```

    For example, in the following image, the AzDevOps branch **old-branch** will be deleted from AzDevOps. Replace **branch_name** with the name of the AzDevOps branch you want to delete.

    !['Git push delete branch' command in the 'VSC Terminal'](../assets/images/09-branches/delete/azdev/del-branch-vsc-005a.png)

    A message in the **VSC Terminal** confirms that the branch is deleted from AzDevOps.

    !['Git push delete remote branch' confirmation message the 'VSC Terminal'](../assets/images/09-branches/delete/azdev/del-branch-vsc-005b.png)

You've deleted a branch using VSC successfully.

## Delete a branch using AzDevOps {#azdev-delete-branch}

Complete the following steps to delete a branch using AzDevOps.

> **Note**: Deleting a branch using AzDevOps removes the branch from AzDevOps only. Your local repo might retain a copy of the branch until you pull updates from AzDevOps into your local repo, or clone the AzDevOps repo again. To delete a branch from your local repo *and* from AzDevOps, follow the steps in [Delete a branch using VSC](#vsc-az-delete-branch).
>

1. Open a web browser, go to the AzDevOps website at [https://dev.azure.com](https://dev.azure.com), and sign in.

2. On the **Projects** tab, locate the project repo with the branch you want to delete, and select the **Repos** icon.

    For example, in the following image, the **Repos** icon for the project **example-repo** is selected.

    ![Example AzDevOps repo project with the 'Repos' icon selected](../assets/images/09-branches/delete/azdev/del-branch-azdev-002.png)

3. Select **Branches** from the left side menu.

    ![Example AzDevOps repo project with the 'Branches' icon selected](../assets/images/09-branches/delete/azdev/del-branch-azdev-003.png)

4. Select the vertical ellipsis (**`⋮`**) icon beside the branch you want delete (on the right side), and then choose **Delete branch**.

    For example, in the following image, the branch named **old-branch** will be deleted.

    ![alt text](../assets/images/09-branches/delete/azdev/del-branch-azdev-004a.png)

    If you're prompted to confirm the deletion, select **Delete**.

    ![alt text](../assets/images/09-branches/delete/azdev/del-branch-azdev-004b.png)

5. The message **You updated \<deleted-branch\> just now** indicates that the branch has been deleted from AzDevOps.

    For example, in the following image, the message **You updated old-branch just now** indicates that the branch named **old-branch** is deleted from AzDevOps.

    ![alt text](../assets/images/09-branches/delete/azdev/del-branch-azdev-005.png)

You've deleted a branch using AzDevOps successfully.

{% include appendices.html %}
