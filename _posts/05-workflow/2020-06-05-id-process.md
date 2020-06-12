---
layout: multi
title: Instructional design review process
subtitle: GitHub
description: An overview of the Instructional design review process.
author:
date: 01 Jun 2020
post-number: 5.5
category: workflow
position-in-category: 5
include-in-pre-reqs: "false"
include-in-quickstart: "false"
video_url: "none"
---

![Alt image text placeholder](../assets/images/05-workflow/id-process/github/img-placeholder.png)

This guide describes the general **Instructional Design (ID) Review** process for a typical project.

> **Note**: The ID review process described in this guide is generalized and is not intended to capture the process entirely. The process can vary between projects and you should ask your project manager about the specific review processes that apply to the course you are working on.

{% include prerequisites.html %}

## Topics in this guide

- [Topic 1: How an ID review is initiated](#topic1)
- [Topic 2: Steps required to conduct an ID review](#topic2)
- [Topic 3: ID review branch naming convention](#topic3)
- [Topic 4: Key points about the ID review process](#topic4)

{% include video.html %}

## Topic 1: How an ID review is initiated {#topic1}

A content author initiates a review by sending an email to the reviewer to request a review. The author's email provides the following details:

- **Module number**: The module number that the file for review belongs to.
- **File name(s)**: The name of the file(s) to be reviewed.
- **Task type**: The type of review required (i.e. instructional design review, technical review, copy edit, etc.).

## Topic 2: Steps required to conduct an ID review {#topic2}

The following steps are required to conduct a general ID review as part of a typical project.

1. When you receive an email from a content author requesting a review, note the name(s) of the file(s) to be reviewed.

2. Use the Visual Studio Code (VSC) editor to clone the project's remote repo onto your computer by following the guide [Download course files (clone repo)]({{site.baseurl}}/download-files/clone-repo.html). The cloned repo you create on your computer is your **local repo**.

3. Create a new branch in your local repo with VSC using the guide [Create new branch]({{site.baseurl}}/branches/new-branch.html). The new branch is your local **ID review branch**, and should be created from the **master** branch.

    > **Note**: Apply the branch naming convention `m <module number> idreview <id reviewer's surname>` to your new branch, as described in [Topic 3: ID review branch naming convention](#topic3). For example, **m6idreviewlee**.

4. Review some content, apply, save and commit your changes/ corrections in VSC on your ID review branch.

5. Push changes to remote.

    > **Note**: Push to the project's remote repo regularly, e.g. after your review a lesson or single file. Do not wait until full review is complete before pushing.

6. In a web browser, access the course files on GitHub by following the guide [View course files in web browser](
{{site.baseurl}}/download-files/view-in-browser.html).

7. On GitHub, open a new **Pull Request** (PR) by using the guide [Create pull request]({{site.baseurl}}/pull-requests/create-pr.html).

    > **Note**: Keep the new PR open (i.e. do not merge the PR), to allow you to apply any subsequent changes necessitated by the review process. Subsequent changes to the ID review branch will be rolled into the open pull request. Configure the pull request by following the remaining steps in this guide.
    >
    > General information about pull requests is available from the guide [Pull requests overview]({{site.baseurl}}/pull-requests/pr-overview.html).

8. On the GitHub page **Open a pull request**, use the dropdowns to configure the PR branches as follows:
  
    - For **base**, choose the **master** branch
    - For **compare**, select the name of your **id review branch** branch, e.g. **m6idreviewlee**

    <!-- ![Base and compare branch dropdowns for configuring a GitHub pull request](../assets/images/05-workflow/id-process/github/04-pr-branches.png) -->

9. On the GitHub page **Open a pull request**, add the following information into the PR title text field:

    - number of the module that the file under review belongs to
    - type of review you are conducting (e.g. instructional design, technical review, etc.)
    - name of the base/ target branch to merge into

    The following provides an example of a suitable PR title as: **Mod 6 ID review merge into master**

    <!-- ![Example PR title in the PR title text field on GitHub](../assets/images/05-workflow/id-process/github/05-pr-title.png) -->

10. On the GitHub page **Open a pull request**, in the **Write** tab, add a checklist for each item in the file to be reviewed by using the following markdown syntax.

    ```markdown
    - [ ] ID Review Complete
      - [ ] ID Review Complete - Lesson 1
      - [ ] ID Review Issues Resolved - Lesson 1
      - [ ] ID Review Complete - Lesson 2
      - [ ] ID Review Issues Resolved - Lesson 2
      - [ ] ID Review Complete - Lesson 3
      - [ ] ID Review Issues Resolved - Lesson 3
      - [ ] ID Review Complete - Lesson 4
      - [ ] ID Review Issues Resolved - Lesson 4
      - [ ] ID Review Complete - Lab
      - [ ] ID Review Issues Resolved - Lab
    ```

    <!-- ![Checklist for each item in the file to be reviewed inside the Write tab of the GitHub page 'Open a pull request'](../assets/images/05-workflow/id-process/github/06-pr-checklist.png) -->

    > **Note**: Work with the content author to determine the items to be reviewed, like the number of topics or lessons the file under review contains. Each topic, lesson or component of content that the file contains can be added as an item to the checklist in GitHub.

11. On the GitHub page **Open a pull request**, choose **Create pull request**.

    <!-- ![Create pull request button on the GitHub page 'Open a pull request'](../assets/images/05-workflow/id-process/github/07-pr-create.png) -->

12. Review the instructional design of contents of the file(s) on the originating branch in accordance with WayPoint Ventures' guidelines.

13. Keep a record of any proposed corrections/ changes to the content.

14. Notify the content author of any required changes to the content.

15. Work with the content author to determine which proposed corrections are to be applied to the content.

16. When you and the content author have determined the corrections/ changes, apply all required changes to ID review branch in VSC (informed by the author's feedback).

17. Save, stage, commit and push changes to remote repo.

18. Repeat **Step** 14 to 17 until all of the items are addressed and the content passes ID review.

19. When the content passes ID review, delete all comments from the markdown files (not the comments in the pull request).

20. Saves, stage, commit and push all finalized ID review changes

21. In the pull request page on GitHub, confirm that the **this branch has no conflicts with the base branch** message is shown, then select **Merge pull request**.

    <!-- ![Branch has no conflicts with the base branch message, in the pull request page on GitHub](../assets/images/05-workflow/id-process/github/16-tr-merge.png) -->

    > **Note**: If GitHub indicates that there are conflicts, follow the guide [Resolve merge conflicts]({{site.baseurl}}/pull-requests/merge-conflicts.html) to address any outstanding merge issues, and then try merging the pull request again.

22. In the pull request page on GitHub, choose **Confirm merge** to merge the originating branch back into the master branch on the project’s GitHub repo.

    <!-- ![Confirm merge button for merging the originating branch into the master branch on GitHub](../assets/images/05-workflow/id-process/github/17-merge-confirm.png) -->

23. The **Pull request successfully merged and closed** message on GitHub indicates that you have merged the PR successfully.

    <!-- ![Message indicating that the PR has been successfully on GitHub](../assets/images/05-workflow/id-process/github/18-merge-success.png) -->

24. Delete the ID review branch.

25. Send an email to the copy editor.

## Topic 3: ID review branch naming convention {#topic3}

Todo.

## Topic 4: Key points about the ID review process {#topic4}

The following are key points about the ID review process.

<!-- - A **content author** requests a review by sending an email to the reviewer.
- The **ID reviewer**:
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
- The **ID reviewer and content author** work together to identify, agree upon, and add required corrections/ changes to the PR, until the content passes ID review successfully.
- When the content passes ID review, the **ID reviewer** merges the originating branch back into the **master** branch on the project's GitHub repo.

The following diagram provides an overview of the key points in the general ID review process for a typical project.

![Diagram of the ID review process](../assets/images/05-workflow/id-process/github/tr-workflow.png) -->

{% include appendices.html %}

{% include paginator.html %}
