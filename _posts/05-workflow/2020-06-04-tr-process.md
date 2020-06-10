---
layout: multi
title: Technical review process
subtitle: GitHub
description: An overview of the Technical Review process.
author: mkavana
date: 01 Jun 2020
post-number: 5.4
category: workflow
position-in-category: 4
include-in-pre-reqs: "false"
include-in-quickstart: "false"
video_url: "none"
---

This guide describes the general **Technical Review** process for a typical project.

> **Note**: The technical review process described in this guide is generalized and is not intended to capture the process entirely. The process can vary between projects and you should ask your project manager about the specific review processes that apply to the course you are working on.

{% include prerequisites.html %}

## Topics in this guide

- [Topic 1: How a technical review is initiated](#topic1)
- [Topic 2: Steps required to conduct a technical review](#topic2)
- [Topic 3: Key points about the technical review process](#topic3)

{% include video.html %}

## Topic 1: How a technical review is initiated {#topic1}

A content author initiates a review by sending an email to the reviewer to request a review. The author's email provides the following details:

- **Module number**: The module number that the file for review belongs to.
- **Task type**: The type of review required (i.e. technical review, instructional design review, copy edit, etc.).
- **Source branch name**: The name of the branch that the file for review is on. This is also referred to as the **compare** or **originating** branch.
- **Target branch**: The name of the branch that the corrected/ changed file will be merged into, after the review is completed. This is also referred to as the **base** branch, and examples include the **master** or **originating** branch, etc.

> **Note**:  A content author develops content in their own authoring branch, and uses a separate authoring branch for each module. Authoring branches use the naming convention `m <module number> auth <author's surname>`, where:
>
> - The prefix `m` is for “module”.
> - `<module number>` refers to the module number that the file to be reviewed belongs to.
> - `auth` is a short code for "content authoring" i.e. the stage in the process the file is at.
> - The author's `<surname>` is added as a suffix to distinguish the author's work from other contributors.
>
> ### Example authoring branch name
>
> The following explains how the example authoring branch named **m6authlee** is constructed.
>
> - Number of the module the file under review belongs to = **6**.
> - Task short code for content authoring = **auth**.
> - Author's surname = **Lee**.
> - Author's resulting branch name = **m6authlee**.

## Topic 2: Steps required to conduct a technical review {#topic2}

The following diagram and accompanying steps provide an overview of the general technical review process for a typical project.

![Diagram of the technical review process](../assets/images/05-workflow/tr-process/github/img-placeholder.png)

1. Download, install and configure the required software according to the guides in the **Install software** section of the WayPoint Documentation website.

2. When a content author requests a review by sending you an email, note the name of the authoring/ originating branch to be reviewed.

3. Open a web browser, go to [github.com](https://www.github.com) and sign into your GitHub user account.

4. On GitHub, open a new Pull Request.

5. Add the text **[DO NOT MERGE]** to the PR title.

6. Set up the PR as follows:

    - compare branch = authoring/ originating branch
    - base branch = master branch

    > **Note**: Keep the PR open (i.e. do not merge the PR) to allow the content author/ originating branch owner to apply any changes necessitated by the review.
    >
    > **Note**: **????? TBC ?????** When you create a new PR, GitHub will send a notification to the originating branch owner.

7. Review the contents of the file(s) on the originating branch for technical accuracy in accordance with WayPoint Ventures' technical review guidelines.

8. Record any proposed corrections/ changes to the content in the open PR on GitHub.

9. Notify the originating branch owner of any required changes to the content.

10. Work with the content author to determine which corrections proposed in the PR are to be applied.

11. When you and the content author have determined the corrections/ changes to be applied, allow the content author sufficient time to:

    - work through the corrections/ changes proposed in the PR.
    - apply the necessary changes to the content on their originating branch (in VSC).
    - push the corrected/ changed content back to the project's remote repo.
    - notify you that the corrected/ changed content is available from the project's remote repo.

12. Repeat Step 7 to 11 until the content passes technical review successfully.

13. When the content passes technical review, use the open PR to merge the originating branch back into the master branch on the project’s remote repo.

## Topic 3: Key points about the technical review process {#topic3}

- A **content author** requests a review by sending an email to the reviewer.
- The **technical reviewer**:
  - receives an author's email requesting a review.
  - opens a new GitHub Pull Request (PR).
  - adds the text **[DO NOT MERGE]** to the PR title.
  - sets the PR **compare** branch to the originating branch.
  - sets the PR **base** branch to master.
  - keeps the PR open (i.e. does not merge the PR) to allow the originating branch owner to apply changes to the content during the review.
  - reviews the contents of the file(s) on the originating branch.
  - records any proposed changes to the content in the PR.
  - notifies the originating branch owner of any required changes to the content.
- The **content author**/ originating branch owner:
  - works through the corrections/ changes proposed in the PR by the reviewer.
  - applies any necessary changes to the content on their originating branch (in VCS).
  - pushes the corrected/ changed content back to the remote repo.
  - notifies the reviewer that the corrected/ changed content is available from the remote repo.
- The **technical reviewer and content author** work together to identify, agree upon, and add required corrections/ changes to the PR, until the content passes technical review successfully.
- When the content passes technical review, the **technical reviewer** merges the originating branch back into the **master** branch on the project's remote repo.

{% include appendices.html %}

{% include paginator.html %}
