---
layout: multi
title: Authoring process
subtitle: GitHub
description: An overview of the content authoring process.
author: mkavana
date: 01 Jun 2020
post-number: 5.3
category: workflow
position-in-category: 3
include-in-pre-reqs: "false"
include-in-quickstart: "false"
include-in-azdevops-quickstart: "false"
video_url: "none"
---

This guide describes the general content authoring process for a typical project.

> **Note**: The authoring process described in this guide is generalized and is not intended to capture the authoring process entirely. The authoring process can vary between projects and type of review. In this guide, Topic 3 describes [Submitting your content for review](#author-review), and information about specific review processes is available from the guides in the remainder of the **Workflow and processes** section. If you are unsure about the content authoring process, consult your project manager.

{% include prerequisites.html %}

## Topics in this guide

- [Summary of the content authoring process](#author-summary)
- [Authoring branch naming convention](#author-branch)
- [Submitting your content for review](#author-review)
- [Key points about the content authoring process](#author-points)

{% include video.html %}

## Summary of the content authoring process {#author-summary}

The following diagram and accompanying steps provide an overview of the general content authoring process for a typical project.

![Diagram of the content authoring process](../assets/images/05-workflow/author/github/01-author-process.png)

1. Download, install and configure the required software according to the guides in the **Install software** section of the WayPoint Documentation website.

2. Use the Visual Studio Code (VSC) editor to clone the project's remote repo onto your computer by following the guide [Download course files (clone repo)]({{site.baseurl}}/download-files/clone-repo.html). The cloned repo you create on your computer is your **local repo**.

3. Create a new branch in your local repo with VSC using the guide [Create new branch]({{site.baseurl}}/branches/new-branch.html). The new branch is your local **authoring branch**, and should be created from the **master** branch.

    > **Note**: Apply the branch naming convention `m <module number> auth <author's surname>` to your new authoring branch, as described in [Authoring branch naming convention](#author-branch).

4. In VSC, work on your local authoring branch to create a new markdown file or open an existing markdown file to edit.

5. Add your text content and image links into the markdown file. Ensure that your content adheres to the [Markdown syntax guide]({{site.baseurl}}/add-content/syntax.html) as you [Add/ edit markdown in VSC]({{site.baseurl}}/add-content/edit-in-vsc.html).

6. For each new image link you add to the markdown file, upload a corresponding image file (PNG) to the appropriate **media** directory by following the guide [Add/ edit images in VSC]({{site.baseurl}}/add-content/add-images.html).

7. In VSC, save, stage and commit the changes you make to the markdown file on your local authoring branch using the guide [Send (push) files]({{site.baseurl}}/branches/push-files.html).

8. Use VSC to push your local authoring branch (with your file changes) to the project's remote repo, according to the guide [Send (push) files]({{site.baseurl}}/branches/push-files.html).

9. Send an email to the appropriate reviewer requesting a review of the content you pushed to the project's remote repo. [Submitting your content for review](#author-review) provides more details about submitting content for review.

10. The reviewer will create a new **Pull Request** for your new/ modified content in the project's remote repo by using the guide [Create pull request]({{site.baseurl}}/pull-requests/create-pr.html).

    > **Note**: General information about pull requests is available from the guide [Pull requests overview]({{site.baseurl}}/pull-requests/pr-overview.html).

11. When the reviewer responds to your email, follow the guide [Work in a pull request]({{site.baseurl}}/pull-requests/work-in-pr.html) and work with the reviewer to evaluate the reviewer's proposed corrections/ changes to your content, and to determine which corrections/ changes to apply.

12. If necessary, work on your local repo in VSC to apply the content corrections/ changes you agreed with the reviewer.

13. Repeat **Step 4** to **12** for each review type, until you and the reviewer have made all the necessary changes to your content.

14. When all necessary changes have been applied, the reviewer will merge your new/ updated content from your authoring branch into the master branch of the project's remote repo.

## Authoring branch naming convention {#author-branch}

Each author must work in their own authoring branch. A separate authoring branch for each module is also required. This approach keeps the content separated per author, at each stage in the process, and on a module by module basis.

Generally, an author creates an authoring branch from the master branch of the project's remote repo using the guide [Create new branch]({{site.baseurl}}/branches/new-branch.html). When you create a new authoring branch, your branch name should describe your branch's content and make the branch's purpose and owner clear to other contributors. Authoring branches use the following naming convention (all lower case):

`m <module number> auth <author's surname>`:

- The prefix `m` is for “module”.
- `<module number>` refers to the module number that the file to be reviewed belongs to.
- `auth` is a short code for "content authoring" i.e. the stage in the process the file is at.
- The author's `<surname>` is added as a suffix to distinguish the author's work from other contributors.

### Example authoring branch name

The following explains how the example authoring branch name `m6authlee` is constructed.

- `m` is an abbreviation for "module".
- `6` is the number of the module that the file belongs to.
- `auth` is a short code for "content authoring".
- `lee` is a reference to the author's surname.

Putting the previous items together results in the authoring branch name `m6authlee`.

## Submitting your content for review {#author-review}

All content developed for the project must be reviewed at various stages in the project’s life cycle. Most projects require Technical, Educational, Instructional Design and Inclusively reviews, as well as Copy Editing, and Compliance and Plagiarism Testing (among others). Typically, a content author initiates a review by sending an email to the reviewer to request a review. The author's email *must* provide the following details:

- **Module number**: The module number that the file for review belongs to.
- **Task type**: The type of review required (i.e. technical review, instructional design review, copy edit, etc.).
- **Source branch name**: The name of the branch that the file for review is on. This is also referred to as the **compare** or **originating** branch.
- **Target branch**: The name of the branch that the corrected/ changed file will be merged into, after the review is completed. This is also referred to as the **base** branch, and examples include the **master** or **originating** branch, etc.

How and when authors submit their content for review can vary in accordance with a project's requirements and the type of review. For example, changes made during a Technical Review might be applied directly to an author’s branch by the Technical Reviewer. An Instructional Design reviewer might work on their own reviewer branch, created from master, to apply changes to an author's content, and then merge their reviewer’s branch back into master. Furthermore, other reviewers might conduct reviews or apply edits outside of the repo's branches.

> **Note**: Ask your project manager about the specific review processes that apply to the course you are working on. Information about specific review processes is available from the guides in the remainder of the **Workflow and processes** section.

The following diagram exemplifies some of the branching structure required for single module, as part of a typical review process.

![Diagram of the branching structure required for single module, as part of a typical review process](../assets/images/05-workflow/author/github/02-branch-structure.png)

## Key points about the content authoring process {#author-points}

The following points summarize the main aspects of the content authoring process. Clarify the details of how the workflow applies to the course you are working on with your project manager.

- Each author develops content on their own authoring branch.
- An author must create a new authoring branch for each module they work on.
- Authoring branches are created from the master branch of the project's remote repo.
- Authoring branches *must* adhere to the project’s branch naming convention.
- For reviews, all new content and proposed changes to existing content must be added to a pull request (PR).
- Request reviews and get PRs created as soon as you can, to facilitate reviews earlier in the process.
- Authors and reviewers should work together to evaluate and discuss the changes proposed within a pull request.
- Reviewers will merge PRs back into master (or into the author's branch).

The following image illustrates how branching, pull requests and merging apply to the authoring and review processes in general.

![Diagram of the branch, pull request and merging processes](../assets/images/05-workflow/author/github/03-pr-process.png)

{% include appendices.html %}

{% include paginator.html %}
