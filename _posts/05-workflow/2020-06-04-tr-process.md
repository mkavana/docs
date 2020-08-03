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

- [How a technical review is initiated](#tr-summary)
- [Steps required to conduct a technical review](#tr-steps)
- [Key points about the technical review process](#tr-points)

{% include video.html %}

## How a technical review is initiated {#tr-summary}

A content author initiates a review by sending an email to the reviewer to request a review. The author's email provides the following details:

- **Module number**: The module number that the file for review belongs to.
- **Task type**: The type of review required (i.e. technical review, instructional design review, copy edit, etc.).
- **Source branch name**: The name of the branch that the file for review is on. This is also referred to as the **compare** or **originating** branch.
- **Target branch**: The name of the branch that the corrected/ changed file will be merged into, after the review is completed. This is also referred to as the **base** branch, and is typically the **master** branch.

> **Note**:  A content author develops content on their own authoring branch, with a separate authoring branch for each module. Authoring branches use the naming convention `m <module number> auth <author's surname>`, where:
>
> - The prefix `m` is for “module”.
> - `<module number>` refers to the module number that the file to be reviewed belongs to.
> - `auth` is a short code for "content authoring" i.e. the stage in the process the file is at.
> - The author's `<surname>` is added as a suffix to distinguish the author's work from other contributors.
>
> ### Example authoring branch name
>
> The following explains how the example authoring branch name `m6authlee` is constructed.
>
> - `m` is an abbreviation for "module".
> - `6` is the number of the module that the file belongs to.
> - `auth` is a short code for "content authoring".
> - `lee` is a reference to the author's surname.
>
> Putting the previous items together results in the authoring branch name `m6authlee`.

## Steps required to conduct a technical review {#tr-steps}

The following steps are required to conduct a general technical review as part of a typical project.

1. When you receive an email from a content author requesting a review, note the name of the authoring/ originating branch to be reviewed.

2. Access the file(s) to be reviewed on GitHub by following the guide [View course files in web browser](
{{site.baseurl}}/download-files/view-in-browser.html).

3. On GitHub, open a new **Pull Request** (PR) by using the guide [Create pull request]({{site.baseurl}}/pull-requests/create-pr.html).

    > **Note**: Keep the new PR open (i.e. do not merge the PR), to allow the content author/ originating branch owner to apply any changes necessitated by the review. Configure the pull request by following the remaining steps in this guide.
    >
    > General information about pull requests is available from the guide [Pull requests overview]({{site.baseurl}}/pull-requests/pr-overview.html).

4. On the GitHub page **Open a pull request**, use the dropdowns to configure the PR branches as follows:
  
    - For **base**, choose the **master** branch
    - For **compare**, select the name of the originating **authoring** branch, e.g. **m6authlee**

    ![Base and compare branch dropdowns for configuring a GitHub pull request](../assets/images/05-workflow/tr-process/github/04-pr-branches.png)

5. On the GitHub page **Open a pull request**, add the following information into the PR title text field:

    - prefix **[Do not merge]**
    - number of the module that the file under review belongs to
    - type of review you are conducting (e.g. technical review, instructional design, etc.)
    - name of the compare/ originating authoring branch to merge from
    - name of the base/ target branch to merge into

    The following provides an example of a suitable PR title as: **[Do not merge] Mod 6 Tech Review of m6authlee merge into master**

    ![Example PR title in the PR title text field on GitHub](../assets/images/05-workflow/tr-process/github/05-pr-title.png)

6. On the GitHub page **Open a pull request**, in the **Write** tab, add a checklist for each item in the file to be reviewed by using the following markdown syntax.

    ```markdown
    - [ ] Tech Review Complete
      - [ ] Tech Review Complete - Lesson 1
      - [ ] Tech Review Issues Resolved - Lesson 1
      - [ ] Tech Review Complete - Lesson 2
      - [ ] Tech Review Issues Resolved - Lesson 2
      - [ ] Tech Review Complete - Lesson 3
      - [ ] Tech Review Issues Resolved - Lesson 3
      - [ ] Tech Review Complete - Lesson 4
      - [ ] Tech Review Issues Resolved - Lesson 4
      - [ ] Tech Review Complete - Lab
      - [ ] Tech Review Issues Resolved - Lab
    ```

    ![Checklist for each item in the file to be reviewed inside the Write tab of the GitHub page 'Open a pull request'](../assets/images/05-workflow/tr-process/github/06-pr-checklist.png)

    > **Note**: Work with the content author to determine the items to be reviewed, like the number of topics or lessons the file under review contains. Each topic, lesson or component of content that the file contains can be added as an item to the checklist in GitHub.

7. On the GitHub page **Open a pull request**, choose **Create pull request**.

    ![Create pull request button on the GitHub page 'Open a pull request'](../assets/images/05-workflow/tr-process/github/07-pr-create.png)

8. Review the contents of the file(s) on the originating branch for technical accuracy in accordance with WayPoint Ventures' technical review guidelines.

9. Keep a record of any proposed corrections/ changes to the content.

10. Notify the content author of any required changes to the content.<!-- Does this exchange happen by email? -->

11. Work with the content author to determine which proposed corrections are to be applied to the content.

12. When you and the content author have determined the corrections/ changes to be applied, allow the content author sufficient time to:

    - apply the necessary changes to the content on their originating/ authoring branch (in VSC).
    - push their corrected/ changed content back to the project's GitHub repo.
    - notify you that the corrected/ changed content is available from the project's GitHub repo.

13. When the author notifies you that corrections have been applied to an item on the checklist, review the updated content. If a checklist item passes technical review, update the item's corresponding checkbox (in the pull request **Conversation** tab on GitHub) to indicate that the item was addressed and passed.

    ![Checkbox indicating that an item has been addressed, in the pull request 'Conversation' tab on GitHub](../assets/images/05-workflow/tr-process/github/13-tr-checkbox.png)

14. Repeat **Step** 8 to 13 until all of the checklist items are addressed and the content passes technical review.

15. When the content passes technical review, in the pull request **Conversation** tab on GitHub, use the checkbox to indicate that the full technical review has been completed successfully.

    ![Checkbox indicating that the full technical review has been completed successfully, in the pull request 'Conversation' tab on GitHub](../assets/images/05-workflow/tr-process/github/15-tr-complete.png)

16. In the pull request page on GitHub, confirm that the **this branch has no conflicts with the base branch** message is shown, then select **Merge pull request**.<!-- Should the PR be merged or not? -->

    ![Branch has no conflicts with the base branch message, in the pull request page on GitHub](../assets/images/05-workflow/tr-process/github/16-tr-merge.png)

    > **Note**: If GitHub indicates that there are conflicts, follow the guide [Resolve merge conflicts]({{site.baseurl}}/pull-requests/merge-conflicts.html) to address any outstanding merge issues, and then try merging the pull request again.

17. In the pull request page on GitHub, choose **Confirm merge** to merge the originating branch back into the master branch on the project’s GitHub repo.

    ![Confirm merge button for merging the originating branch into the master branch on GitHub](../assets/images/05-workflow/tr-process/github/17-merge-confirm.png)

18. The **Pull request successfully merged and closed** message on GitHub indicates that you have merged the PR successfully.

    > **Note**: *Do not delete* the originating authoring branch.

    ![Message indicating that the PR has been successfully on GitHub](../assets/images/05-workflow/tr-process/github/18-merge-success.png)

## Key points about the technical review process {#tr-points}

The following are key points about the technical review process.

- A **content author** requests a review by sending an email to the reviewer.
- The **technical reviewer**:
  - receives an author's email requesting a review.
  - opens a new GitHub Pull Request (PR).
  - sets the PR **compare** branch to the originating branch.
  - sets the PR **base** branch to master.
  - adds the prefix **[Do not merge]** text, and a suitable description, to the PR title.
  - creates a checklist of items to be addressed.
  - keeps the PR open (i.e. does not merge the PR) to allow the author to apply changes during the review.
  - reviews the contents of the file(s) on the originating branch.
  - records any proposed changes to the content in the PR.
  - notifies the originating branch owner of any required changes to the content.
- The **content author**/ originating branch owner:
  - works through the corrections/ changes proposed by the reviewer.
  - applies any necessary changes to the content on their originating branch (in VSC).
  - pushes the corrected/ changed content back to the project's GitHub repo.
  - notifies the reviewer that the corrected/ changed content is available from the remote repo.
- The **technical reviewer and content author** work together to identify, agree upon, and add required corrections/ changes to the PR, until the content passes technical review successfully.
- When the content passes technical review, the **technical reviewer** merges the originating branch back into the **master** branch on the project's GitHub repo.

The following diagram provides an overview of the key points in the general technical review process for a typical project.

![Diagram of the technical review process](../assets/images/05-workflow/tr-process/github/tr-workflow.png)

{% include appendices.html %}

{% include paginator.html %}
