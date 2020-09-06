---
layout: multi
title: Merge a pull request
subtitle: AzDevOps
description: A guide to using a merge commit to merge changes from an AzDevOps PR into a branch
author: eamonnk, mkavana
date: 01 Jun 2020
post-number: 13.4
#category: pull-requests
#position-in-category: 4
include-in-pre-reqs: "false"
include-in-quickstart: "false"
video_url: "https://web.microsoftstream.com/embed/video/3b533444-94f5-46c5-97f8-52d8fca5c81c?autoplay=false&amp;showinfo=true"
---

This guide describes how to use a merge commit to combine the changes from a Pull Request (PR) into a branch on AzDevOps.

> **Note**: This guide assumes you've an open AzDevOps PR that contains the changes you want to merge, and that you know the number of the AzDevOps PR you're merging.

{% include prerequisites.html %}

## Topics in this guide

- [Examples of when to use an AzDevOps merge commit](#az-merge-examples)
- [Merge an AzDevOps PR](#az-merge-steps)

{% include video.html %}

## Examples of when to use an AzDevOps merge commit {#az-merge-examples}

This topic provides examples of when to use a merge commit to merge an AzDevOps PR.

When all your file changes are implemented, and you've opened an AzDevOps PR for your changes, the files in the AzDevOps PR *must* be merged back into the originating branch (like the master or authoring branch) using a merge commit.

The following are examples of when to use a merge commit to merge an AzDevOps PR.

### Authors

As part of the content authoring process, an author might create a new authoring branch from the **master** branch. When the author has finished developing content, the changes applied to the files on the authoring branch *must* be merged back into the master branch. The author pushes the files on their authoring branch "up" to AzDevOps. Then, an AzDevOps PR is created to request merging the authoring branch back into master. When the proposed file changes within the AzDevOps PR have been approved by an AzDevOps reviewer, the contents of the AzDevOps PR are combined with the contents of the master branch using an AzDevOps merge commit.

### Reviewers

During the review process, a reviewer might modify an author's content. To compartmentalize the reviewer's changes, the reviewer might create a reviewer's branch based on the **originating author's branch**. When the reviewer has finished making changes, the reviewer's branch *must* be merged back into the originating author's branch. An AzDevOps PR is created to request combining the reviewer's branch with the originating author's branch. When the changes have been approved by an AzDevOps reviewer, the contents of the AzDevOps PR are combined with the contents of the originating author's branch using an AzDevOps merge commit.

> **Note**: Beyond the examples cited in this guide, the steps described in [Merge an AzDevOps PR](#az-merge-steps) can be applied to combine files from an AzDevOps PR with files on a branch (like master) using an AzDevOps merge commit.
>
> AzDevOps merge commit operations are usually performed by a *designated Waypoint team member* who is responsible for merging AzDevOps PRs. Your project manager can identify the appropriate Waypoint team member for you.
>

### Handoff email

When an AzeDevOps PR is ready to be merged, the person who created the PR *must* send an email to the Waypoint team member responsible for merging AzDevOps PRs.

The email *must* state the following information:

- **Module number**. The number of the module/ unit that the AzDevOps PR to be merged relates to.
- **Task type**. The task performed on the files in the PR (for example, *ID review*, *content authoring*, etc.).
- **AzDevOps PR number**. The number of the AzDevOps PR to be merged or a link to the PR.
- **Merging branch name**. The name of the branch that the files are being merged *from*. For example, the name of your author's/ reviewer's branch or a link to the PR.
- **Target branch**. The name of the branch the files are being merged *into*. For example, **master** or the name of an originating author's branch or a link to the PR.
- **Confirmation**. Confirmation that all file changes have been implemented, the files have been reviewed, and the PR is ready to be merged into the originating branch.

## Merge an AzDevOps PR {#az-merge-steps}

The **Waypoint team member responsible for merging AzDevOps PRs** will complete the following steps to merge an AzDevOps PR.

1. Open a web browser, go to the AzDevOps website at [https://dev.azure.com](https://dev.azure.com), and sign in.

    ![AzDevOps homepage](../assets/images/13-pull-requests/merge-pr/azdev/az-pr-mrg-02-001.png)

2. On the **Projects** tab, locate the project repo you require, and select the **Repos** icon.

    For example, in the following image, the **Repos** icon for the project **example-repo** is selected.

    ![Example AzDevOps repo project with the 'Repos' icon selected](../assets/images/13-pull-requests/merge-pr/azdev/az-pr-mrg-02-002.png)

3. Select **Pull requests** from the left side menu.

    ![Example AzDevOps repo with the 'Pull requests' menu item selected](../assets/images/13-pull-requests/merge-pr/azdev/az-pr-mrg-02-003.png)

4. In the **Pull requests** pane, on the right side, choose the **Active** tab for a list of open PRs. Then, select the PR you want to open merge.

    For example, in the following image, the PR **merge from ce branch \*\*mkavana-mod01-ce\*\* into \*\*master\*\*** is selected from the list of open PRs in the **Active**  tab.

    ![Example AzDevOps repo with a single PR selected](../assets/images/13-pull-requests/merge-pr/azdev/az-pr-mrg-02-004.png)

5. Select the **Files** tab.

    ![Example AzDevOps PR with the 'Files' tab selected](../assets/images/13-pull-requests/merge-pr/azdev/az-pr-mrg-02-005a.png)

    > **Note**: Resolve any active comments, indicated by **Active (0)**, by adding comment text, and choosing **Reply & resolve**. For example, in the following image, the resolving comment text **Resolving comment to close PR** is added.
    >
    > ![Example AzDevOps PR with a sample resolving commented added](../assets/images/13-pull-requests/merge-pr/azdev/az-pr-mrg-02-005b.png)
    >

6. Set the **Complete** dropdown option to **Complete**, and then select the **Complete** dropdown/ button.

    > **Note**: Ask the branch owner to approve merging the PR into their branch, if you're merging into a branch that requires the branch owner to approve merge operations. For example, merging into **master** usually requires the branch owner's approval.  
    >

    ![Example AzDevOps PR with the 'Complete' dropdown option set to 'Complete'](../assets/images/13-pull-requests/merge-pr/azdev/az-pr-mrg-02-006.png)

7. In the **Complete pull request** pane, set the following (default) values, and then select **Complete merge**.

   - Set the **Merge type** dropdown option to **Merge (no fast-forward)**.
   - Set the checkbox to enable **Complete associated work items after merging**.
   - Set the checkbox to enable  **Delete the review branch after merging**
   - Set the checkbox to disable **Customize merge commit message** and accept the default comment. Alternatively (optional), enable **Customize merge commit message**, and then enter a descriptive comment for your merge action.

    > **Note**: Ask the owner of the branch you're merging *from* to confirm that you can delete their branch *after the PR's been merged*.
    >

    ![The 'Complete pull request' pane in an example AzDevOps PR](../assets/images/13-pull-requests/merge-pr/azdev/az-pr-mrg-02-007.png)

8. Ensure the status of the PR changes to **Competed** (in green), to confirm that the merge is complete.

    ![Example AzDevOps PR with a status of 'Completed'](../assets/images/13-pull-requests/merge-pr/azdev/az-pr-mrg-02-008.png)

You've merged an AzDevOps PR successfully.

> **Note**: The new/ updated files merged from the PR are present in destination branch. A merged PR is accessible from the **Completed** tab in the **Pull requests** pane.
>

{% include appendices.html %}
