---
layout: multi
title: Content editing process
subtitle: GitHub
description:
author:
date: 01 Jun 2020
post-number: 5.6
category: workflow
position-in-category: 6
include-in-pre-reqs: "false"
include-in-quickstart: "false"
video_url: "none"
---
<!--todo:
  - add answers to questions in comments below
  - proof read (check for misplaced references to 'id process')
  - check integrity of hyperlinks
-->

This guide describes the general **Content Editing (CE) Review** process for a typical project.

> **Note**: The CE review process described in this guide is generalized and is not intended to capture the process entirely. The process can vary between projects and you should ask your project manager about the specific review processes that apply to the course you are working on.

{% include prerequisites.html %}

## Topics in this guide

- [Topic 1: How a CE review is initiated](#topic1)
- [Topic 2: Steps required to conduct a CE review](#topic2)
- [Topic 3: CE review branch naming convention](#topic3)
- [Topic 4: Key points about the CE review process](#topic4)

{% include video.html %}

## Topic 1: How a CE review is initiated {#topic1}

An Instructional Design (ID) reviewer initiates a CE review by sending an email to the CE reviewer to request a CE review. An CE review is usually requested when the ID reviewer has completed an ID review of content for a course module. The ID reviewer's email provides the following details:

- **GitHub username**. The ID reviewer's GitHub account username.
- **Module number** The module number that the file(s) for review belong(s) to.
- **File name** The name(s) of the file(s) to be reviewed.
- **Task type**. The type of review required (i.e. CE review).

The file(s) for CE review should be on the master branch of the project's GitHub (remote) repo.

## Topic 2: Steps required to conduct a CE review

The following steps are required to conduct a general CE review as part of a typical project.

1. When you receive an email from an ID reviewer requesting a CE review, note the name(s) of the file(s) to be reviewed.

2. Use the Visual Studio Code (VSC) editor to clone the project's GitHub repo onto your computer by following the guide [Download course files (clone repo)]({{site.baseurl}}/download-files/clone-repo.html). The cloned repo you create on your computer is your **local repo**.

3. Create a new branch in your local repo with VSC using the guide [Create new branch]({{site.baseurl}}/branches/new-branch.html). The new branch is your local **CE review branch**, and should be created from the **master** branch in VSC.

    > **Note**: Apply the branch naming convention `m <module number> cereview <ce reviewer's surname>` to your new branch, as described in [Topic 3: CE review branch naming convention](#topic3). For example, **m6-cereview-lee**.
    >

4. In VSC, on your local **CE review branch**, open the first markdown file for review, and review the contents of the file according to WayPoint Ventures' guidelines.

5. In VSC, apply, save, stage, and commit any necessary changes/ corrections you make to the markdown file by using the guide [Send (push) branch]({{site.baseurl}}/branches/push-branch.html).

6. Push the file containing your changes to GitHub by following the guide [Send (push) branch]({{site.baseurl}}/branches/push-branch.html).

    > **Note**: Push to GitHub regularly, e.g. after you have reviewed a lesson or single file. *Do not wait* until you have reviewed *all* of the files before pushing to GitHub.

7. In a web browser, access the project's GitHub repo by following the guide [View course files in web browser]({{site.baseurl}}/download-files/view-in-browser.html).

8. On GitHub, open a new **Pull Request** (PR) by using the guide [Create pull request]({{site.baseurl}}/pull-requests/create-pr.html).

    > **Note**: Keep the new PR open (i.e. *do not merge* the PR yet). Keeping the PR open allows you to apply subsequent changes necessitated by the review process. Any further changes you make to the files on your CE review branch that you push to GitHub will be rolled into the open pull request. Configure the pull request by following the remaining steps in this guide.
    >
    > General information about pull requests is available from the guide [Pull requests overview]({{site.baseurl}}/pull-requests/pr-overview.html).
    >

9. On the GitHub page **Open a pull request**, use the dropdowns to configure the PR branches as follows:
  
    - For **base**, choose the **master** branch.
    - For **compare**, select the name of your **CE review branch** branch (e.g. **m6-cereview-lee**).

    ![Branch configuration on the GitHub 'Open a pull request' page](../assets/images/05-workflow/ce-process/github/09-pr-branches.png)

10. On the GitHub page **Open a pull request**, add the following into the PR **title text entry field**:

    - number of the module the file you reviewed belongs to
    - type of review you conducted (i.e. CE review)
    - name of the base branch to merge into (i.e. master)

    For example, a suitable PR title is: **Mod 6 CE review merge into master**

    ![PR title text field on the GitHub 'Open a pull request' page](../assets/images/05-workflow/ce-process/github/10-pr-title.png)

11. **Optional**: On the GitHub page **Open a pull request**, in the **Write** tab, add a checklist for each item to be reviewed by entering the following markdown syntax into the **text entry field**.

    ```markdown
    - [ ] CE Review Complete
        - [ ] CE Review Complete - Lesson 1
        - [ ] CE Review Issues Resolved - Lesson 1
        - [ ] CE Review Complete - Lesson 2
        - [ ] CE Review Issues Resolved - Lesson 2
        - [ ] CE Review Complete - Lesson 3
        - [ ] CE Review Issues Resolved - Lesson 3
        - [ ] CE Review Complete - Lab
        - [ ] CE Review Issues Resolved - Lab
    ```

    ![Checklist in the 'Write' tab on the GitHub 'Open a pull request' page](../assets/images/05-workflow/ce-process/github/11-pr-checklist.png)

    > **Note**: An item in your GitHub checklist can be a single topic, lesson or file (as appropriate). If necessary, consult the ID reviewer to determine a suitable approach to dividing the module content into GitHub checklist items.
    >
    > Checklists provide a convenient way for reviewers, content authors, and other contributors to track the progress of a review. Checklists are *optional*; reviewers are *not required* to use checklists on GitHub.
    >

12. From the right side menu of the GitHub page **Open a pull request**, in the **Reviewers** section, select the **gear icon**. In the **text entry field**, enter the ID reviewer's GitHub username. Then, choose the ID reviewer's GitHub username from the list to add the ID reviewer as a GitHub reviewer to the PR.

    The following image shows adding the GitHub user **eamonnk** to the PR.

    ![GitHub username in the add reviewer text entry field on the GitHub 'Open a pull request' page](../assets/images/05-workflow/ce-process/github/12-pr-add-reviewer-a.png)

    The following image shows the GitHub user **eamonnk** added as a reviewer to the PR.

    ![GitHub user added as a reviewer to a PR on the GitHub 'Open a pull request' page](../assets/images/05-workflow/ce-process/github/12-pr-add-reviewer-b.png)

    > **Note**: When you add a GitHub user as a reviewer to the PR (like an ID reviewer), GitHub will send the GitHub user a notification each time a change is made to the pull request (for example, when a file in the PR is edited or added).
    >
    > At this stage, the **ID reviewer**:
    >
    > - clones the GitHub repo
    > - switches to your CE review branch
    > - evaluates the file containing your CE review changes
    >
    > Where necessary, the ID reviewer will add comments about your CE review changes to the open PR, or by sending you an email. Comments are only required when an ID reviewer seeks clarification about your CE review changes; accepted changes do not require comments.
    >
    > An ID reviewer can add the originating content author as a GitHub reviewer to your open PR or as a carbon copy (CC) email recipient. The content author *must* only add comments to the open PR in GitHub or by email. The author *must not* edit the content editor's branch, or create a new authoring branch to make changes.
    >

13. On the GitHub page **Open a pull request**, choose **Create pull request**.

    ![Create pull request button on the GitHub 'Open a pull request' page](../assets/images/05-workflow/ce-process/github/13-pr-create.png)

14. If necessary, consult the ID reviewer (and content author) about the changes you made to the file on your CE review branch.
    <!-- Does CE or ID apply edits to files based on feedback? -->
    > **Note**: Reviewers and authors can communicate in the following ways (among others) to discuss changes to content necessitated by a review:
    >
    > - face-to-face meeting, video or voice call
    > - comments added to the **Conversation** tab on the GitHub pull requests page
    > - markdown comments inside a markdown file, formatted using the correct markdown syntax for comments described in the [Markdown syntax guide]({{site.baseurl}}/add-content/syntax.html)
    > - email exchanges
    >

15. On your CE review branch in VSC, open the next file for review and conduct a CE review of the file's contents.

16. In VSC, apply any required changes/ corrections to the file on your local CE review branch. If necessary, apply any further changes/ corrections to the previous file in accordance with feedback from the ID reviewer (and author).
    <!-- Does CE or ID apply edits to files? -->

17. On your CE review branch in VSC, save, stage, commit and push your changes to GitHub by using the guide [Send (push) branch]({{site.baseurl}}/branches/push-branch.html).

18. Repeat **Step** 14 to 17 until all of the files for review have passed your CE review. Each time you push new changes, the ID reviewer (and author) may evaluate your corrections and provide feedback.

    > **Note**: If you created a GitHub checklist, indicate when each item on the GitHub checklist has been addressed, and when the review has been completed, by using the checkboxes in the **Conversation** tab on the GitHub pull requests page.

    ![Checklist in the 'Conversation' tab on the GitHub 'Open a pull request' page indicating a review has been completed](../assets/images/05-workflow/ce-process/github/18-checklist-complete.png)

19. When all files have passed CE review, send an email to the ID reviewer indicating that your CE review has been completed.
    <!-- Does CE or ID merge CE's branch, delete CE branch and handoff to Test? -->
    > **Note**: The **ID reviewer** will complete the process by:
    >
    > - merging your CE branch into master using the open GitHub PR
    > - deleting your CE branch
    > - notifying the Test team by email that you have completed your CE review successfully
    >

## Topic 3: CE review branch naming convention

Each reviewer must work in their own reviewer's branch. A separate reviewer branch for each module is also required. This approach keeps the content separated per reviewer, at each stage in the process, and on a module by module basis.

Generally, a reviewer creates a reviewer's branch from the master branch of the project's GitHub repo using the guide [Create new branch]({{site.baseurl}}/branches/new-branch.html). When you create a new reviewer's branch, your branch name should describe your branch's content and make the branch's purpose and owner clear to other contributors.

CE reviewers' branches use the following naming convention (all lower case):

`m <module number> cereview <reviewer's surname>`:

- The prefix `m` is for “module”.
- `<module number>` refers to the module number that the file to be reviewed belongs to.
- `cereview` is a short code for "content editing review" i.e. the stage in the process the file is at.
- The reviewer's `<surname>` is added as a suffix to distinguish the reviewer's work from other contributors.

### Example CE reviewer's branch name

The following explains how the example reviewer branch name `m6-cereview-lee` is constructed.

- `m` is an abbreviation for "module".
- `6` is the number of the module that the file(s) for review belong(s) to.
- `cereview` is a short code for "content editing review".
- `lee` is a reference to the reviewer's surname.

Putting the previous items together results in the reviewer branch name `m6-cereview-lee`.

## Topic 4: Key points about the CE review process

The following diagram provides an overview of key points in the general CE review process for a typical project.

![Diagram of the content editing review process](../assets/images/05-workflow/ce-process/github/19-ce-workflow.png)

The following are key points about the content editing review process.

- **Instructional Design reviewer (ID)** requests content editing review by email (when content for a module is ready).

- **Content editor (CE)**:

  - clone's project's GitHub repo
  - creates local "CE review" branch from master in VSC
  - reviews content in VSC on CE review branch
  - applies, saves and commits necessary changes/ corrections in VSC (on CE review branch)
  - pushes changes/ corrections to GitHub
  - creates pull request (PR) to merge CE branch into master
  - adds ID reviewer to PR as a reviewer on GitHub
  - liaises with ID reviewer to implement ID's (and authors) feedback on CE reviewer's changes until all files pass CE review
  - signs off on PR with finalized files by email to ID reviewer

- **ID reviewer**:

  - evaluates files in PR as CE adds changes
  - liaises with CE (and author) to provide feedback on CE reviewer's changes
  - when all files pass CE, ID merges CE branch into master using (CE's open PR)
  - deletes merged CE branch
  - signs off on files passed CE review by sending an email to Test team

{% include appendices.html %}

{% include paginator.html %}
