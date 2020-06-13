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

<!--
  Todo:
    - Resolve issues/ questions in the comments in this topic section.
    - Verify the steps are accurate.
    - Add images and alt text, on path:
        ![Alt image text placeholder](../assets/images/05-workflow/id-process/github/img-placeholder.png)
    - Check for broken links
-->

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

A content author initiates a review by sending an email to the reviewer to request an ID review. The author's email provides the following details:

- **Module number**: The module number that the file(s) for review belong(s) to.
- **File name**: The name of the file(s) to be reviewed.
- **Task type**: The type of review required (i.e. instructional design review).

The file for review should be on the master branch of the project's GitHub (remote) repo.

## Topic 2: Steps required to conduct an ID review {#topic2}

The following steps are required to conduct a general ID review as part of a typical project.

1. When you receive an email from a content author requesting a review, note the name(s) of the file(s) to be reviewed.

2. Use the Visual Studio Code (VSC) editor to clone the project's GitHub repo onto your computer by following the guide [Download course files (clone repo)]({{site.baseurl}}/download-files/clone-repo.html). The cloned repo you create on your computer is your **local repo**.

3. Create a new branch in your local repo with VSC using the guide [Create new branch]({{site.baseurl}}/branches/new-branch.html). The new branch is your local **ID review branch**, and should be created from the **master** branch in VSC.

    > **Note**: Apply the branch naming convention `m <module number> idreview <id reviewer's surname>` to your new branch, as described in [Topic 3: ID review branch naming convention](#topic3). For example, **m6-idreview-lee**.

4. In VSC, on your local **ID review branch**, open the first markdown file for review, and review the contents of the file in VSC according to WayPoint Ventures guidelines.
   <!-- Does ID make note of changes in .md file, PR or email? -->

5. In VSC, apply, save, stage, and commit your necessary changes/ corrections to the markdown file using the guide [Upload your changes]({{site.baseurl}}/branches/push-changes.html).

6. Push the file containing your changes to GitHub by following the guide [Upload your changes]({{site.baseurl}}/branches/push-changes.html).

    > **Note**: Push to GitHub regularly, e.g. after review a lesson or single file. *Do not wait* until you have reviewed *all* of the files before pushing to GitHub.

7. In a web browser, access the project's GitHub repo by following the guide [View course files in web browser]({{site.baseurl}}/download-files/view-in-browser.html).

8. On GitHub, open a new **Pull Request** (PR) by using the guide [Create pull request]({{site.baseurl}}/pull-requests/create-pr.html).

    > **Note**: Keep the new PR open (i.e. *do not merge* the PR yet). Keeping the PR open allows you to apply subsequent changes necessitated by the review process. Any further changes you make to the files on your ID review branch that you push to GitHub will be rolled into the open pull request. Configure the pull request by following the remaining steps in this guide.
    >
    > General information about pull requests is available from the guide [Pull requests overview]({{site.baseurl}}/pull-requests/pr-overview.html).

9. On the GitHub page **Open a pull request**, use the dropdowns to configure the PR branches as follows:
  
    - For **base**, choose the **master** branch.
    - For **compare**, select the name of your **ID review branch** branch, e.g. **m6-idreview-lee**.

10. On the GitHub page **Open a pull request**, add the following into the PR title text field:

    - number of the module the reviewed file belongs to
    - type of review you are conducting (i.e. instructional design)
    - name of the base branch to merge into (i.e. master)

    For example, a suitable PR title is: **Mod 6 ID review merge into master**

11. On the GitHub page **Open a pull request**, in the **Write** tab, add a checklist for each item to be reviewed using the following markdown syntax.
    <!-- Is a GitHub checklist used by an ID -->

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

    > **Note**: Add a topic, lesson or file as a checklist item in GitHub. If necessary, consult the content author to determine suitable items to add to the checklist.

12. On the GitHub page **Open a pull request**, choose **Create pull request**.

13. Notify the content author of the name of the file you reviewed, and the name of your ID review branch.
    <!-- Where does ID record proposed corrections/ changes to the content -->
14. Ask the content author to evaluate the changes you made to the file on your ID review branch. Allow the content author sufficient time to:

    - evaluate your changes
    - provide you with feedback on your changes

15. While you wait for the author's feedback, on your ID review branch in VSC, open the next file for review and conduct an ID review of the file's contents.

16. On your ID review branch in VSC, apply any required changes/ corrections to file. If necessary, apply any further changes/ corrections to the previous file in accordance with the author's feedback.
    <!-- Where do ID and author exchange their communications, e.g. email? -->
17. On your ID review branch in VSC, save, stage, commit and push your changes to GitHub.

18. Repeat Step 14 to 18 until all of the files for review have passed ID review. Notify the content author each time you push new changes to allow the author to evaluate your corrections and provide feedback.
    <!-- If a checklist is used in GitHub, check items off the list -->
19. When all content for review passes ID review, in VSC, delete any comments from within the markdown files (*do not delete* comments from the pull request on GitHub).

20. On your ID review branch in VSC, save, stage, commit and push the passed files to GitHub (i.e. the files that contain your finalized ID review changes).

21. On GitHub, go to PR you opened and merge your ID review branch into master by following the guide [Merge a pull request]({{site.baseurl}}/pull-requests/merge-pr.html).

22. On GitHub, delete your ID review branch using the guide [Delete branch]({{site.baseurl}}/branches/delete-branch.html).

23. Notify the author and copy editor (by email) that you have completed your ID review.

## Topic 3: ID review branch naming convention {#topic3}

<!-- Todo: 
  - Verify the following steps.
-->

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

The following are key points about the ID review process.

<!-- Todo: 
  - Create and add summary process diagram.
-->

- **Author** requests ID review by email.

- **ID reviewer**:

  - clone's project's GitHub repo
  - creates local review branch from master in VSC
  - reviews content in VSC on ID review branch
  - applies, saves and commits necessary changes/ corrections in VSC (on ID review branch)
  - pushes changes/ corrections to GitHub
  - creates pull request (PR) to merge ID review branch into master
  - notifies author when PR's ready for evaluation

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
