---
layout: multi
title: Recover deleted branch
subtitle: AzDevOps
description: Guide to restoring a deleted branch using AzDevOps
author: mkavana
date: 01 Jun 2020
post-number: 9.8
#category: branches
#position-in-category: 8
include-in-pre-reqs: "false"
include-in-quickstart: "false"
include-in-azdevops-quickstart: "false"
video_url: "none"
---

This guide describes how to restore a deleted branch using AzDevOps.

> **Note**: The following instructions *only* apply to restoring a branch that was on AzDevOps previously, and then deleted using AzDevOps. The process for restoring branches deleted by other means, or local branches, is beyond the scope of this guide.
>
> You *must* know the name of the branch you want to recover.
>
> As an example, this guide restores a deleted branch named **old-branch** to a sample AzDevOps repository **example-repo**. Modify the following instructions to suit your preferred AzDevOps repository (repo).
>

{% include prerequisites.html %}

## Topics in this guide

- [Restore a deleted branch to AzDevOps](#az-restore-branch)

{% include video.html %}

## Restore a deleted branch to AzDevOps {#az-restore-branch}

Complete the following steps to restore a deleted branch to AzDevOps.

1. Open a web browser, go to the AzDevOps website at [https://dev.azure.com](https://dev.azure.com), and sign in.

2. On the **Projects** tab, locate the project repo with the branch you want to restore, and select the **Repos** icon.

    For example, in the following image, the **Repos** icon for the project **example-repo** is selected.

    ![Example AzDevOps repo project with the 'Repos' icon selected](../assets/images/09-branches/recover/azdev/restore-branch-002.png)

3. Select **Branches** from the left side menu.

    ![Example AzDevOps repo project with the 'Branches' icon selected](../assets/images/09-branches/recover/azdev/restore-branch-003.png)

4. In the search box, upper right side, enter the name of the deleted branch you want to recover.

    For example, in the following image, the name of the deleted branch **old-branch** is entered into the search box.

    ![Example AzDevOps repo project with the name of a branch to restore entered into the search box](../assets/images/09-branches/recover/azdev/restore-branch-004.png)

5. In the **Deleted branches** pane, select the vertical ellipsis (**`⋮`**) icon beside the branch you want recover (on the right side), and then choose **Restore branch**.

    For example, in the following image, the **Restore branch** option is selected for the deleted branch named **old-branch**.

    ![Example AzDevOps repo project with the 'Restore branch' option selected](../assets/images/09-branches/recover/azdev/restore-branch-005.png)

6. The message **Successfully restored \<branch_name\>** indicates that the branch is recovered successfully.

    The recovered branch is now available from the **Branches** pane, under the **All** tab.

    For example, in the following image, the message **Successfully restored old-branch** indicates that the branch named **old-branch** is recovered successfully. In the following image, the branch **old-branch** is listed in the **Branches** pane, under the **All** tab.

    ![Example AzDevOps repo project with the 'Successfully restored branch...' message](../assets/images/09-branches/recover/azdev/restore-branch-006.png)

You've recovered a branch using AzDevOps successfully.

{% include appendices.html %}
