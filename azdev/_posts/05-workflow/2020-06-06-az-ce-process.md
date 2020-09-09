---
layout: multi
title: Content edit process
subtitle: AzDevOps
description: A guide to the Content Editing (CE) Review process
author: eamonnk, mkavana
date: 01 Jun 2020
post-number: 5.6
#category: workflow
#position-in-category: 6
include-in-pre-reqs: "false"
include-in-quickstart: "false"
include-in-azdevops-quickstart: "false"
video_url: "none"
---

This guide describes the general **Content Editing (CE) Review** process for a typical project.

> **Note**: The CE review process described in this guide is generalized, and is not intended to capture the process entirely. The process can vary between projects. You should ask your project manager about the specific review processes that apply to the project you're working on.
>

{% include prerequisites.html %}

## Topics in this guide

- [How a CE review is initiated](#az-ce-overview)
- [Steps required to conduct a CE review](#az-ce-steps)
- [CE review branch naming convention](#az-ce-branching)
- [Key points about the CE review process](#az-ce-points)

{% include video.html %}

## How a CE review is initiated {#az-ce-overview}

An Instructional Design (ID) reviewer usually initiates a CE review by sending an email to the CE reviewer to request a CE review. A CE review is typically requested when the ID reviewer has completed an ID review of content for a course module. The ID reviewer's email provides the CE reviewer with the following details:

- **AzDevOps username**. The ID reviewer's AzDevOps account username.
- **Module number** The module number that the file(s) for review belong(s) to.
- **File name** The name(s) of the file(s) to be reviewed.
- **Task type**. The type of review required (i.e. CE review).

> **Note**: Files for CE review are usually on the master branch of the project's AzDevOps repository (remote repo). However, depending on the project's requirements, the files for CE review might be on another branch, like an authoring branch. If you're unsure, ask your project manager.
>

## Steps required to conduct a CE review {#az-ce-steps}

The following steps are required to conduct a general CE review as part of a typical project.

1. When you receive an email from an ID reviewer requesting a CE review, note the names of the files to be reviewed, and the name of the branch that the files are on.

2. Use the Visual Studio Code (VSC) editor to download (or "clone") the project's AzDevOps repo onto your computer by following the guide [Download course files (clone repo)]({{site.baseurl}}/download-files/clone-repo.html). The cloned repo you create on your computer is your **local repo**.

    > **Note**: If you already have a local repo with the course files, update the contents of your local repo using the `git pull` command by following the guide [Update branch (pull)]({{site.baseurl}}/branches/pull-updates.html).
    >

3. In VSC, create a new CE reviewer's branch by selecting the branch icon from the VSC **status bar** (bottom left), and choose **+ Create new branch from...**.

    ![The 'Branch' icon in the VSC status bar, and the 'Create new branch' menu option](../assets/images/05-workflow/ce-process/azdev/az-ce-003.png)

4. Enter a name for your CE reviewer's branch.

    > **Note**: Apply the branch naming convention `m <module number> cereview <ce reviewer's surname>` to your new branch, as described in [CE review branch naming convention](#az-ce-branching).
    >

    For example, in the following image, the new CE reviewer's branch is named **m5-cereview-kelly**.

    ![Example new reviewer's branch in VSC](../assets/images/05-workflow/ce-process/azdev/az-ce-004.png)

5. In the prompt to **Select a ref to create the `<CE reviewer's>` branch from**, choose a branch that your CE reviewer's branch will be based on.

    For example, in the following image, the CE reviewer's branch named **m5-cereview-kelly** is based on the authoring branch named **m5authsmith**.

    ![The 'Create branch from...' menu option in VSC](../assets/images/05-workflow/ce-process/azdev/az-ce-005.png)

6. Verify that the VSC **status bar** indicates that VSC has switched focus to your new CE reviewer's branch.

    For example, in the following image, the VSC status bar indicates that VSC is switched to the CE reviewer's branch named **m5-cereview-kelly**.

    ![VSC status bar indicating that VSC has switched focus to example CE reviewer's branch](../assets/images/05-workflow/ce-process/azdev/az-ce-006.png)

7. In VSC, on your local **CE review branch**, open the first markdown file for review, and review the file's contents according to WayPoint Ventures' guidelines.

8. In VSC, apply, save, stage, and commit any necessary changes/ corrections you make to the markdown file by using the guide [Send (push) files]({{site.baseurl}}/branches/push-files.html).

9. Upload (or push) the file containing your changes to AzDevOps by following the guide [Send (push) files]({{site.baseurl}}/branches/push-files.html).

    > **Note**: Push to AzDevOps regularly, for example after you've reviewed a suitable unit of content, like a lesson or module. *Do not wait* until you've reviewed *all* of the files before pushing.
    >

10. Verify that the edited file you pushed is on AzDevOps.

    In a web browser, access the project's AzDevOps repo by following the guide [View course files in web browser]({{site.baseurl}}/download-files/view-in-browser.html).

    In AzDevOps, select **Repos** > **Files**, and use the dropdown to choose your CE reviewer's branch. Go to the file you pushed, and verify that the file contains your changes/ corrections.

    ![Example CE reviewer's branch open on AzDevOps](../assets/images/05-workflow/ce-process/azdev/az-ce-010.png)

11. In AzDevOps, open a new pull request (PR).

    Select **Repos**, then choose **Pull requests**, and select **New pull request**.

    > **Note**: Keep the new PR open (i.e. *do not merge* the PR yet). Keeping the PR open allows you to apply subsequent changes necessitated by the review process. If you make further changes to the files on your CE review branch, and push them to AzDevOps, the changes will be "rolled into" the open PR.
    >
    > General information about PRs is available from the guide [Pull requests overview]({{site.baseurl}}/pull-requests/pr-overview.html).
    >

    ![The 'New pull request' button on AzDevOps](../assets/images/05-workflow/ce-process/azdev/az-ce-011.png)

12. On the **New pull request** page, add the following information to configure the PR, and when you've finished, choose **Create**.

    - **Source and Destination branches**: Set the dropdowns to merge your **CE reviewer's branch** *into* **master branch**. Some projects require merging the CE reviewer's branch into the originating author's branch. Ask your project manager which branch to merge into. For example, in the following image, the PR is set to merge the CE reviewer's branch named **m5-cereview-kelly** into the authoring branch named **m5authsmith**.
    - **Title**: The PR's title should describe the PRs purpose. For example, **mod 5 CE review on branch m5-cereview-kelly branch merge into author branch m5authsmith.**. To describe the PRs purpose, add the following information into the PR **title** text field:
      - number of the module that the file you're reviewing belongs to
      - type of review you're conducting (i.e. ce review)
      - name of the ce reviewer's branch you're merging *from*
      - name of branch to merge *into*
    - **Description**: Enter a brief description of the PR. For example, **content updates from ce review**.
    - **Reviewers** : Select the ID reviewer's AzDevOps username, and add the AzDevOps usernames of any other reviewers or relevant stakeholders (like the originating content author).

    ![The 'New pull request' configuration page on AzDevOps](../assets/images/05-workflow/ce-process/azdev/az-ce-012.png)

13. Propose or discuss a change/ correction using comments.

    Select **Repos**, then choose **Pull requests**, and select the PR you created in steps **11** and **12**.

    ![Example pull request open in AzDevOps](../assets/images/05-workflow/ce-process/azdev/az-ce-013a.png)

    In the **Pull request**, go to the **Overview** tab, choose **Add a comment...**, enter a description of your proposed change, and select **Comment**.

    > **Note**: To view comments added to a PR by another contributor on AzDevOps, open the PR in AzDevOps, go to the **Files** tab, and select a file that contains comments.
    >
    > ![Example file with comments open in AvDevOps](../assets/images/05-workflow/ce-process/azdev/az-ce-013b.png)
    >
    > View the comments in the file by selecting the **Comments down arrow**. From the dropdown menu, choose **Active**.
    >
    > ![The 'Active comments' dropdown menu in AzDevOps](../assets/images/05-workflow/ce-process/azdev/az-ce-013c.png)
    >
    > Reply to a comment by entering text into the box **Write a reply**, and then choose **Reply**.
    >
    > ![Example reply to a comment in AzDevOps](../assets/images/05-workflow/ce-process/azdev/az-ce-013d.png)
    >
    > To close a comment, select **Reply & Resolve**.
    >

14. Notify the ID reviewer when you've applied corrections/ changes to the file's contents or added a comment to the PR.

    If necessary, consult the ID reviewer (and content author) about the changes you made to the file on your CE review branch.

    > **Note**: Reviewers and authors can communicate in the following ways (among others) to discuss changes to content necessitated by a review:
    >
    > - face-to-face meeting, video or voice call
    > - comments added to the **Overview** tab on the AzDevOps pull requests page
    > - markdown comments inside a markdown file, formatted using the correct markdown syntax for comments described in the [Markdown syntax guide]({{site.baseurl}}/add-content/syntax.html)
    > - email exchanges
    >

15. On your CE review branch in VSC, open the next file for review and review the file's contents.

16. In VSC, apply any required changes/ corrections to the file on your local CE review branch, and add/ reply to comments to the PR on AzDevOps. If necessary, apply any further changes/ corrections to the previous file in accordance with feedback from the ID reviewer (and content author).

17. On your CE review branch in VSC, save, stage, commit, and push your changes to AzDevOps by using the guide [Send (push) files]({{site.baseurl}}/branches/push-files.html).

18. Repeat steps **13** to **17** until all of the files for review have passed your CE review. Each time you push new changes, the ID reviewer and author might evaluate your corrections and provide feedback.

19. When all content for review has passed CE review, in VSC, delete any comments from within the markdown files (*do not delete* open comments from the pull request page on AzDevOps).

20. On your CE review branch in VSC, save, stage, commit, and push the passed files to AzDevOps (i.e. the files that contain your finalized changes).

    > **Note**: For some projects, an ID reviewer might complete the following steps **21** to **23** (rather than the CE reviewer). Ask your project manager about the CE review process for the project you're working on.
    >

21. To merge your CE review changes, go to AzDevOps, open the PR, select the dropdown **Complete**, and then choose the menu option **Complete**.

    ![The 'Complete' dropdown menu in a example 'Pull requests' page on AzDevOps](../assets/images/05-workflow/ce-process/azdev/az-ce-021.png)

22. In the **Complete pull request** pane, leave the default values. If available, enable the option to **Delete `<CE reviewer's>` branch after merging**, and then choose **Complete merge**.

    ![The 'Compete pull request' pane in AzDevOps](../assets/images/05-workflow/ce-process/azdev/az-ce-022.png)

23. Notify the ID reviewer and the Test team by email that you've completed your CE review.

You've conducted a general CE review as part of a typical project successfully.

## CE review branch naming convention {#az-ce-branching}

Each reviewer must work in their own reviewer's branch. A separate reviewer branch for each module/ unit of content is also required. This approach keeps the content separated per reviewer, at each stage in the process, and on a module by module basis.

Generally, a reviewer creates a reviewer's branch from the master branch of the project's AzDevOps repo using the guide [Create new branch]({{site.baseurl}}/branches/new-branch.html). However, depending on the project’s requirements, the files for review might be on another branch, like an authoring branch. If you’re unsure, ask your project manager.

When you create a new reviewer's branch, your branch name should describe your branch's content and make the branch's purpose, and owner, clear to other contributors.

CE reviewers' branches use the following naming convention (all lower case):

`m <module number> cereview <reviewer's surname>`:

- The prefix `m` is for “module”.
- `<module number>` refers to the module number that the file to be reviewed belongs to.
- `cereview` is a short code for "content edit review" i.e. the stage in the process the file is at.
- The reviewer's `<surname>` is added as a suffix to distinguish the reviewer's work from other contributors.

### Example CE reviewer's branch name

The following explains how the example CE reviewer branch name `m6-cereview-lee` is constructed.

- `m` is an abbreviation for "module".
- `6` is the number of the module that the file(s) for review belong(s) to.
- `cereview` is a short code for "content edit review".
- `lee` is a reference to the CE reviewer's surname.

Putting the previous items together results in the CE reviewer branch name `m6-cereview-lee`.

## Key points about the CE review process {#az-ce-points}

The following diagram provides an overview of key points in the general CE review process for a typical project.

![Diagram of the content edit review process](../assets/images/05-workflow/ce-process/azdev/az-ce-025-workflow.png)

The following are key points about the CE review process.

- **Instructional Design reviewer (ID)** requests a Content Editing review by email (usually when content for a module is ready).

- **Content editor (CE)**:

  - clone's the project's AzDEvOps repo
  - creates a local "CE review" branch in VSC
  - reviews content in VSC on CE review branch
  - applies, saves, and commits necessary changes/ corrections in VSC (on CE review branch)
  - pushes changes/ corrections to AzDevOps
  - creates a pull request (PR) to merge CE branch (usually into master)
  - adds ID reviewer to PR as a reviewer on AzDevOps
  - implements feedback from ID reviewer (and author) regarding CE review changes, until all files pass CE review
  - "hands off" PR with finalized files by email to ID reviewer

- **ID reviewer**:

  - evaluates files in PR as CE adds changes/ corrections
  - liaises with CE (and author) to provide feedback on CE reviewer's changes

- **CE** or **ID reviewer** (varies between projects):  

  - when all files pass CE, merges CE branch into master (using CE's open PR)
  - deletes merged CE branch
  - "hands off" passed files to Test team via email

{% include appendices.html %}
