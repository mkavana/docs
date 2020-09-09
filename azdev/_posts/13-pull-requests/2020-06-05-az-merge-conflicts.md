---
layout: multi
title: Resolve merge conflicts
subtitle: AzDevOps
description: A guide to resolving merge conflicts on AzDevOps
author: mkavana, eamonnk
date: 01 Jun 2020
post-number: 13.5
#category: pull-requests
#position-in-category: 5
include-in-pre-reqs: "false"
include-in-quickstart: "false"
include-in-azdevops-quickstart: "false"
video_url: "none"
---

This guide describes merge conflicts, and how to check for merge conflicts in an AzDevOps pull request (PR).

> **Note**: Unlike GitHub, *you cannot resolve merge conflicts in an AzDevOps PR using a web browser*. You must use Visual Studio Code (VSC) instead. To check an AzDevOps PR for merge conflicts, refer to [Check for merge conflicts on AzDevOps](#az-merge-conflict-check). Then, use VSC to resolve the merge conflicts by referring to [Resolve merge conflicts](https://docs.microsoft.com/azure/devops/repos/git/merging?view=azure-devops&tabs=visual-studio#resolve-merge-conflicts-1).
>

{% include prerequisites.html %}

## Topics in this guide

- [An overview of merge conflicts](#az-merge-conflict-overview)
- [Check for merge conflicts on AzDevOps](#az-merge-conflict-check)

{% include video.html %}

## An overview of merge conflicts {#az-merge-conflict-overview}

Git users can work in the same file on different branches concurrently. For example, two Git users working on different branches can modify **line number 100** in the file **example \.md**, at the same time, in their respective local clones of a project repo. Each Git user can then push their modified file "up" to AzDevOps.

Merge conflicts arise from attempts to merge branches that contain incompatible versions of the same file. Staying with the previous example, there is different content on **line number 100** in the file **example \.md** on each of the two users' branches. Pushing the files to AzDevOps creates two competing versions of the file  **example \.md**. When you try to merge the branches, Git doesn't know which version of the file to merge. The result is an error called a "merge conflict".

### About complex and simple merge conflicts

Resolving a merge conflict requires "human intervention" to tell Git/ AzDevOps which version of the file to merge. All merge conflicts *must* be resolved before AzDevOps will allow you to merge a PR.

On AzDevOps, if you attempt to merge a PR with conflicting files, AzDevOps displays a warning message, lists the conflicting files, and deactivates the **Complete** button for merging the PR. The **Complete** button remains deactivated until you've resolved the merge conflicts in VSC.

For example, in the following image, there is a merge conflict warning on an AzDevOps PR for the file **sample-file \.md** and the **Complete** button is deactivated.

![Merge conflict warning on an AzDevOps PR](../assets/images/13-pull-requests/conflicts/azdev/az-pr-conflict-01-001.png)

> **Note**: For more information about merge conflicts, refer to the Microsoft Azure DevOps Documentation page [Resolve merge conflicts](https://docs.microsoft.com/azure/devops/repos/git/merging?view=azure-devops&tabs=visual-studio), and the GitHub documentation page [About merge conflicts](https://docs.github.com/github/collaborating-with-issues-and-pull-requests/about-merge-conflicts).
>

There are many causes of merge conflicts. For complex merge conflicts, you must identify the cause of the conflict and implement an appropriate solution. To resolve a complex merge conflict, refer to the Microsoft Azure DevOps Documentation page [Resolve merge conflicts](https://docs.microsoft.com/azure/devops/repos/git/merging?view=azure-devops&tabs=command-line#resolve-merge-conflicts-1), and to the GitHub documentation page [Resolving a merge conflict using the command line](https://docs.github.com/github/collaborating-with-issues-and-pull-requests/resolving-a-merge-conflict-using-the-command-line).

Competing line changes, like in the previous example, are a common cause of simple merge conflicts. To check an AzDevOps PR for merge conflicts, refer to [Check for merge conflicts on AzDevOps](#az-merge-conflict-check). Then, use VSC to resolve simple merge conflicts by referring to [Resolve merge conflicts](https://docs.microsoft.com/azure/devops/repos/git/merging?view=azure-devops&tabs=visual-studio#resolve-merge-conflicts-1)

## Check for merge conflicts on AzDevOps {#az-merge-conflict-check}

Complete the following steps to check an AzDevOps PR for merge conflicts.

1. Open a web browser, go to the AzDevOps website at [https://dev.azure.com](https://dev.azure.com), and sign in.

    ![AzDevOps homepage](../assets/images/13-pull-requests/conflicts/azdev/az-pr-conflict-02-001.png)

2. On the **Projects** tab, locate the project repo you require, and select the **Repos** icon.

    For example, in the following image, the **Repos** icon for the project **example-repo** is selected.

    ![Example AzDevOps repo project with the 'Repos' icon selected](../assets/images/13-pull-requests/conflicts/azdev/az-pr-conflict-02-002.png)

3. Select **Pull requests** from the left side menu.

    ![Example AzDevOps repo with the 'Pull requests' menu item selected](../assets/images/13-pull-requests/conflicts/azdev/az-pr-conflict-02-003.png)

4. In the **Pull requests** pane, on the right side, choose the **Active** tab for a list of open PRs.

    The **Conflicts** message indicates PRs with merge conflicts. Select a PR for details about the merge conflicts.

    For example, in the following image, the PR **user-01 update sample file** with merge conflicts is selected.

    ![Example AzDevOps PR with a merge conflicts](../assets/images/13-pull-requests/conflicts/azdev/az-pr-conflict-02-004.png)

5. The PR **Overview** tab lists the number of merge conflicts and the names of the conflicting files.

    For example, in the following image, in there is **1 merge conflict** listed for the file **sample-file \.md**.

    ![Example AzDevOps PR with 1 merge conflict and conflicting file](../assets/images/13-pull-requests/conflicts/azdev/az-pr-conflict-02-005.png)

6. Use VSC to resolve the merge conflicts by referring to [Resolve merge conflicts](https://docs.microsoft.com/azure/devops/repos/git/merging?view=azure-devops&tabs=visual-studio#resolve-merge-conflicts-1).

    ![The Microsoft docs article 'Resolve merge conflicts'](../assets/images/13-pull-requests/conflicts/azdev/az-pr-conflict-02-006.png)

You've checked an AzDvOps PR for merge conflict successfully.

{% include appendices.html %}
