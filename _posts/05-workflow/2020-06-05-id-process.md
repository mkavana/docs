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

A content author initiates a review by sending an email to the reviewer to request an ID review. An ID review is usually requested when the author has completed content for a course module. The author's email provides the following details:

- **GitHub username**. The content author's GitHub account username.
- **Module number** The module number that the file(s) for review belong(s) to.
- **File name** The name(s) of the file(s) to be reviewed.
- **Task type**. The type of review required (i.e. ID review).

The file(s) for review should be on the master branch of the project's GitHub (remote) repo.

## Topic 2: Steps required to conduct an ID review {#topic2}

The following steps are required to conduct a general ID review as part of a typical project.

1. When you receive an email from a content author requesting a review, note the name(s) of the file(s) to be reviewed.

2. Use the Visual Studio Code (VSC) editor to clone the project's GitHub repo onto your computer by following the guide [Download course files (clone repo)]({{site.baseurl}}/download-files/clone-repo.html). The cloned repo you create on your computer is your **local repo**.

3. Create a new branch in your local repo with VSC using the guide [Create new branch]({{site.baseurl}}/branches/new-branch.html). The new branch is your local **ID review branch**, and should be created from the **master** branch in VSC.

    > **Note**: Apply the branch naming convention `m <module number> idreview <id reviewer's surname>` to your new branch, as described in [Topic 3: ID review branch naming convention](#topic3). For example, **m6-idreview-lee**.

4. In VSC, on your local **ID review branch**, open the first markdown file for review, and review the contents of the file according to WayPoint Ventures' guidelines.

5. In VSC, apply, save, stage, and commit any necessary changes/ corrections you make to the markdown file by using the guide [Upload your changes]({{site.baseurl}}/branches/push-changes.html).

6. Push the file containing your changes to GitHub by following the guide [Upload your changes]({{site.baseurl}}/branches/push-changes.html).

    > **Note**: Push to GitHub regularly, e.g. after you have reviewed a lesson or single file. *Do not wait* until you have reviewed *all* of the files before pushing to GitHub.

7. In a web browser, access the project's GitHub repo by following the guide [View course files in web browser]({{site.baseurl}}/download-files/view-in-browser.html).

8. On GitHub, open a new **Pull Request** (PR) by using the guide [Create pull request]({{site.baseurl}}/pull-requests/create-pr.html).

    > **Note**: Keep the new PR open (i.e. *do not merge* the PR yet). Keeping the PR open allows you to apply subsequent changes necessitated by the review process. Any further changes you make to the files on your ID review branch that you push to GitHub will be rolled into the open pull request. Configure the pull request by following the remaining steps in this guide.
    >
    > General information about pull requests is available from the guide [Pull requests overview]({{site.baseurl}}/pull-requests/pr-overview.html).

9. On the GitHub page **Open a pull request**, use the dropdowns to configure the PR branches as follows:
  
    - For **base**, choose the **master** branch.
    - For **compare**, select the name of your **ID review branch** branch, e.g. **m6-idreview-lee**.

    ![Branch configuration on the GitHub 'Open a pull request' page](../assets/images/05-workflow/id-process/github/09-pr-branches.png)

10. On the GitHub page **Open a pull request**, add the following into the PR **title text entry field**:

    - number of the module the file you reviewed belongs to
    - type of review you conducted (i.e. ID review)
    - name of the base branch to merge into (i.e. master)

    For example, a suitable PR title is: **Mod 6 ID review merge into master**

    ![PR title text field on the GitHub 'Open a pull request' page](../assets/images/05-workflow/id-process/github/10-pr-title.png)

11. **Optional**: On the GitHub page **Open a pull request**, in the **Write** tab, add a checklist for each item to be reviewed by entering the following markdown syntax into the **text entry field**.

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

    ![Checklist in the 'Write' tab on the GitHub 'Open a pull request' page](../assets/images/05-workflow/id-process/github/11-pr-checklist.png)

    > **Note**: An item in your GitHub checklist can be a single topic, lesson or file (as appropriate). If necessary, consult the content author to determine a suitable approach to dividing the module content into GitHub checklist items.
    >
    > Checklists provide a convenient way for ID reviewers, content authors, and other contributors to track progress of an ID review. Checklists are *optional*; ID reviewers are *not required* to use checklists on GitHub.

12. From the right side menu of the GitHub page **Open a pull request**, in the **Reviewers** section, select the **gear icon**. In the **text entry field**, enter the content author's GitHub username. Then, choose the author's GitHub username from the list to add the author as a reviewer to the PR.

    The following image shows adding the GitHub user **eamonnk** to the PR.

    ![GitHub username in the add reviewer text entry field on the GitHub 'Open a pull request' page](../assets/images/05-workflow/id-process/github/12-pr-add-reviewer-a.png)

    The following image shows the GitHub user **eamonnk** added as a reviewer to the PR.

    ![GitHub user added as a reviewer to a PR on the GitHub 'Open a pull request' page](../assets/images/05-workflow/id-process/github/12-pr-add-reviewer-b.png)

    > **Note**: When you add a GitHub user as a reviewer to the PR (like a content author), GitHub will send the GitHub user a notification each time a change is made to the pull request (for example, when a file in the PR is edited or added).

13. On the GitHub page **Open a pull request**, choose **Create pull request**.

    ![Create pull request button on the GitHub 'Open a pull request' page](../assets/images/05-workflow/id-process/github/13-pr-create.png)

14. If necessary, consult the content author about the changes you made to the file on your ID review branch.

    > **Note**: Reviewers and authors can communicate in the following ways (among others) to discuss changes to content necessitated by a review:
    >
    > - face-to-face meeting, video or voice call
    > - comments added to the **Conversation** tab on the GitHub pull requests page
    > - markdown comments inside a markdown file, formatted using the correct markdown syntax for comments described in the [Markdown syntax guide]({{site.baseurl}}/add-content/syntax.html)
    > - email exchanges
    >

15. On your ID review branch in VSC, open the next file for review and conduct an ID review of the file's contents.

16. In VSC, apply any required changes/ corrections to file on your local ID review branch. If necessary, apply any further changes/ corrections to the previous file in accordance with feedback from the content author.

17. On your ID review branch in VSC, save, stage, commit and push your changes to GitHub by using the guide [Upload your changes]({{site.baseurl}}/branches/push-changes.html).

18. Repeat **Step** 14 to 17 until all of the files for review have passed your ID review. Each time you push new changes, the author may evaluate your corrections and provide feedback.

    > **Note**: If you created a GitHub checklist, indicate when each item on the GitHub checklist has been addressed, and when the review has been completed, by using the checkboxes in the **Conversation** tab on the GitHub pull requests page.

    ![Checklist in the 'Conversation' tab on the GitHub 'Open a pull request' page indicating a review has been completed](../assets/images/05-workflow/id-process/github/18-checklist-complete.png)

19. When all content for review has passed ID review, in VSC, delete any comments from within the markdown files (*do not delete* comments from the pull request on GitHub).

20. On your ID review branch in VSC, save, stage, commit and push the passed files to GitHub (i.e. the files that contain your finalized changes).

21. On GitHub, go to the **Pull requests** tab for the (open) PR. Confirm that the **this branch has no conflicts with the base branch** message is shown. Choose **Merge pull request** to begin merging your ID review branch into master by following the guide [Merge a pull request]({{site.baseurl}}/pull-requests/merge-pr.html).

    ![Merge pull request button on the GitHub 'pull requests' page](../assets/images/05-workflow/id-process/github/21-pr-merge.png)

    > **Note**: If GitHub indicates that there *are* conflicts, follow the guide [Resolve merge conflicts]({{site.baseurl}}/pull-requests/merge-conflicts.html) to address any outstanding merge issues, and then try merging the pull request again.

22. On the GitHub **Pull requests** tab, select **Confirm merge** to merge your ID review branch into master.

    ![Confirm merge button on the GitHub 'pull requests' tab](../assets/images/05-workflow/id-process/github/22-pr-confirm-merge.png)

23. When the message **Pull request successfully merged and closed** indicates that the PR has merged, select **Delete branch** to delete your ID review branch by following the guide [Delete branch]({{site.baseurl}}/branches/delete-branch.html).

    ![Delete branch button on the GitHub 'pull requests' tab](../assets/images/05-workflow/id-process/github/23-pr-delete-branch.png)

24. Notify the copy editor by email (and the content author) that you have completed your ID review successfully.

## Topic 3: ID review branch naming convention {#topic3}

Each reviewer must work in their own reviewer's branch. A separate reviewer branch for each module is also required. This approach keeps the content separated per reviewer, at each stage in the process, and on a module by module basis.

Generally, a reviewer creates a reviewer's branch from the master branch of the project's GitHub repo using the guide [Create new branch]({{site.baseurl}}/branches/new-branch.html). When you create a new reviewer's branch, your branch name should describe your branch's content and make the branch's purpose and owner clear to other contributors.

ID reviewers' branches use the following naming convention (all lower case):

`m <module number> idreview <reviewer's surname>`:

- The prefix `m` is for “module”.
- `<module number>` refers to the module number that the file to be reviewed belongs to.
- `idreview` is a short code for "instructional design review" i.e. the stage in the process the file is at.
- The reviewer's `<surname>` is added as a suffix to distinguish the reviewer's work from other contributors.

### Example authoring branch name

The following explains how the example reviewer branch name `m6-idreview-lee` is constructed.

- `m` is an abbreviation for "module".
- `6` is the number of the module that the file(s) for review belong(s) to.
- `idreview` is a short code for "instructional design review".
- `lee` is a reference to the reviewer's surname.

Putting the previous items together results in the reviewer branch name `m6-idreview-lee`.

## Topic 4: Key points about the ID review process {#topic4}

The following diagram provides an overview of key points in the general ID review process for a typical project.

![Diagram of the instructional design review process](../assets/images/05-workflow/id-process/github/25-id-workflow.png)

The following are key points about the ID review process.

- **Author** requests ID review by email (when content for a module is ready).

- **ID reviewer**:

  - clone's project's GitHub repo
  - creates local review branch from master in VSC
  - reviews content in VSC on ID review branch
  - applies, saves and commits necessary changes/ corrections in VSC (on ID review branch)
  - pushes changes/ corrections to GitHub
  - creates pull request (PR) to merge ID review branch into master
  - adds author to PR as a reviewer on GitHub

- **Author** evaluates pull request, and liaises with ID to provide feedback on ID reviewer's changes

- **ID reviewer**

  - liaises with author to implement author's feedback on ID reviewer's changes
  - completes ID review
  - deletes comments from markdown files
  - saves, stages, commits and pushes finalized ID review files to open PR
  - merges ID review branch into GitHub master branch
  - deletes the ID review branch
  - notifies the copy editor when ID review is completed

{% include appendices.html %}

{% include paginator.html %}
