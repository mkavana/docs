---
layout: multi
title: Create pull request
subtitle: AzDevOps
description: A guide to creating a pull request on AzDevOps
author: mkavana
date: 01 Jun 2020
post-number: 13.2
#category: pull-requests
#position-in-category: 2
include-in-pre-reqs: "false"
include-in-quickstart: "false"
video_url: "https://web.microsoftstream.com/embed/video/76a6d02d-a51e-4c98-b41c-1f0a115eea5e?autoplay=false&amp;showinfo=true"
---

This guide describes how to create a Pull Request (PR) on AzDevOps.

> **Note**: This guide assumes that any additions/ changes you made to a file in your local repo have been saved, staged, committed, and pushed to AzDevOps using the guide [Send (push) files]({{site.baseurl}}/branches/push-files.html).
>
> General information about PRs is available from the guide [Pull requests overview]({{site.baseurl}}/pull-requests/pr-overview.html).
>

{% include prerequisites.html %}

## Topics in this guide

- [Create a pull request on AzDevOps](#create-pr-azdev)

{% include video.html %}

## Create a pull request on AzDevOps {#create-pr-azdev}

Complete the following steps to create a PR on AzDevOps.

1. Open a web browser, go to the AzDevOps website at [https://dev.azure.com](https://dev.azure.com), and sign in.

    ![AzDevOps user login webpage](../assets/images/13-pull-requests/create-pr/azdev/create-pr-001.png)

2. On the **Projects** tab, locate the project repo with the branch you want to restore, and select the **Repos** icon.

    For example, in the following image, the **Repos** icon for the project **example-repo** is selected.

    ![Example AzDevOps repo project with the 'Repos' icon selected](../assets/images/13-pull-requests/create-pr/azdev/create-pr-002.png)

3. Select **Branches** from the left side menu.

    ![Example AzDevOps repo project with the 'Branches' icon selected](../assets/images/13-pull-requests/create-pr/azdev/create-pr-003.png)

4. In the **Branches** pane, select the vertical ellipsis (**`⋮`**) icon beside the branch you want merge *from* (on the right side), and then choose **New pull request**.

    For example, in the following image, the new PR will be merged from the branch named **mkavana-mod01-ce**.

    ![Example AzDevOps repo project with the 'New pull request' option selected](../assets/images/13-pull-requests/create-pr/azdev/create-pr-004.png)

5. In the **New pull request** form, add the following into the PR **Title** text field:

    - number of the module that the file you're merging belongs to
    - type of action you performed on the file you're merging (for example, content edit review, image updates)
    - name of the branch you're merging *into* (for example, master)

    For example, in the following image, a suitable PR title is **Merge from ce branch mkavana-mod01-ce into master**.

    ![Example PR title on the AzDevOps 'New pull request' page](../assets/images/13-pull-requests/create-pr/azdev/create-pr-005.png)

6. **Optional** In the **Description** text field, describe the file additions/ changes you're merging.

    For example, in the following image, a suitable description is **Merge copy edits from ce branch mkavana-mod01-ce into master with copy edits to the files /sample-folder/sample-file.md**.

    ![Example description on the AzDevOps 'New pull request' page](../assets/images/13-pull-requests/create-pr/azdev/create-pr-006.png)

    > **Note**: Descriptions provide a way for contributors to explain the changes they applied to files on AzDevOps. Descriptions are *optional*, but recommended.
    >
    > The reviewer's guides in the **Workflow and processes** section of this website suggest adding a checklist of items the for review into the **Description** field. A checklist provides a convenient way for reviewers, content authors, and other contributors to track the progress of a review. To add a review checklist, choose a guide that corresponds to your role from the **navigation menu** on the left of this website.
    >

7. In the **Reviewers** pane, in PR **Overview** tab, to add a reviewer to your PR, select **Add**, choose **Required reviewer**, and then enter the reviewer's AzDevOps username.

    In the **Reviewers** pane, add AzDevOps username of the owner of the branch you're merging into, like the originating author for example. If you modify files in the PR, AzDevOps will send notifications to the reviewers you added.

   ![The 'Reviewers' pane in an example pull request tab on AzDevOps](../assets/images/13-pull-requests/create-pr/azdev/create-pr-007.png)

8. Send an email to the person you're handing your files off to (as a notification that your PR is ready). Your email should include the following:

   - Details about the PR (like the names of the branches the PR involves, PR title, number, and purpose). For example, **Mod 01 PR#23 to merge copy edit changes from ce-branch-X into author-branch-Y**
   - URL/ link to the PR on AzDevOps
   - **Optional** screen capture/ grab of the PR

You've created a pull request on AzDevOps successfully.

> **Note**: Keep the new PR open (i.e. do not merge the PR yet). Keeping the PR open allows you to apply and push subsequent changes from your local branch “up” to AzDevOps. Any further changes that you push from your local branch up to AzDevOps will be “rolled into” your open pull request.
>
> At this stage, the reviewer evaluates the file that contains your additions/ changes.
>
> Where necessary, the reviewer will add comments about your changes to the open PR, or by sending you an email. Adding comments to a PR is useful for discussing changes, sharing suggestions, and consulting the reviewer about the changes you made to the file on your branch. To evaluate a reviewer’s feedback in a PR, follow the guide [Work in a pull request]({{site.baseurl}}/pull-requests/work-in-pr.html).
>

{% include appendices.html %}
