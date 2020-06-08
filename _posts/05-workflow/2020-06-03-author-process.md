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
video_url: "none"
---

This guide describes the general content authoring process for a typical project.

> **Note**: The authoring process described in this guide is generalized and is not intended to capture the authoring process entirely. The authoring process can vary between projects and type of review. Information about specific review processes is available from the guides in the remainder of the **Workflow and processes** section. If you are unsure about the content authoring process, consult your project manager.

{% include prerequisites.html %}

## Topics in this guide

- [Topic 1: Summary of the content authoring process](#topic1)

{% include video.html %}

## Topic 1: Summary of the content authoring process {#topic1}

The following diagram and accompanying steps provide an overview of the general content authoring process for a typical project.

![Diagram of the content authoring process](../assets/images/05-workflow/author/github/author-process.png)

1. Download, install and configure the required software according to the guides in the **Install software** section of the WayPoint Documentation website.

2. Use the Visual Studio Code (VSC) editor to clone the project's remote repo onto your computer by following the guide [Download course files (clone repo)]({{site.baseurl}}/download-files/clone-repo.html). The cloned repo you create on your computer is your **local repo**.

3. Create a new branch in your local repo with VSC using the guide [Create new branch]({{site.baseurl}}/branches/new-branch.html). The new branch is your local **authoring branch**, and should be created from the **master** branch.

4. In VSC, work on your local authoring branch to create a new markdown file or open an existing markdown file to edit.

5. Add your text content and image links into the markdown file. Ensure that your content adheres to the [Markdown syntax guide]({{site.baseurl}}/add-content/syntax.html) as you [Add/ edit markdown in VSC]({{site.baseurl}}/add-content/edit-in-vsc.html).

6. For each new image link you add to the markdown file, upload a corresponding image file (PNG) to the appropriate **media** directory by following the guide [Add/ edit images in VSC]({{site.baseurl}}/add-content/add-images.html).

7. In VSC, save, stage and commit the changes you make to the markdown file on your local authoring branch using the guide [Upload your changes]({{site.baseurl}}/branches/push-changes.html).

8. Use VSC to push your local authoring branch (with your file changes) to the project's remote repo, according to the guide [Upload your changes]({{site.baseurl}}/branches/push-changes.html).

9. Send an email to the appropriate reviewer requesting a review of the content you pushed to the project's remote repo.

10. The reviewer will create a new **Pull Request** for your new/ modified content in the project's remote repo by using the guide [Create pull request]({{site.baseurl}}/pull-requests/create-pr.html).

    > **Note**: General information about pull requests is available from the guide [Pull requests overview]({{site.baseurl}}/pull-requests/pr-overview.html).

11. When the reviewer responds to your email, follow the guide [Work in a pull request]({{site.baseurl}}/pull-requests/work-in-pr.html) and work with the reviewer to evaluate the reviewer's proposed corrections/ changes to your content, and to determine which corrections/ changes to apply.

12. If necessary, work on your local authoring branch in VSC to apply the content corrections/ changes you agreed with the reviewer.

13. Repeat **Step 4** to **12** until you and the reviewer have made all the necessary changes to your content.

14. When all necessary changes have been applied, the reviewer will merge your new/ updated content from your authoring branch into the master branch of the project's remote repo.

{% include appendices.html %}

{% include paginator.html %}
