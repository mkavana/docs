---
layout: page
title: Pull requests overview
subtitle:
description: An overview of pull requests
author: mkavana
date: 01 Jun 2020
post-number: 13.1
category: pull-requests
position-in-category: 1
include-in-pre-reqs: "true"
include-in-quickstart: "false"
include-in-azdevops-quickstart: "false"
video_url: "none"
---

This guide provides an overview of pull requests.

> **Note**: The overview of pull requests in this guide is a summary of [Using pull requests to share your work]({{site.baseurl}}/workflow/terminology.html/#using-prs) from the previous guide [Terminology and concepts]({{site.baseurl}}/workflow/terminology.html).
>

{% include prerequisites.html %}

## Topics in this guide

- [An overview of pull requests](#pr-overview)

{% include video.html %}

## An overview of pull requests {#pr-overview}

The following provides an overview of pull requests.

Whenever you add or edit files on a branch in your local repo, save, stage and commit your changes with Visual Studio Code (VSC). You *must* also send (or **push**) the changes you made "up" to the project's remote repository on GitHub or Azure DevOps. The changes you push up to the project's remote repository (repo) *must* then be added (or **merged**) back into the originating branch. For example, changes pushed from an author's or reviewer's local branch can be merged back into the **master branch** on GitHub or Azure DevOps.

![Diagram of how a single git branch relates to master](../assets/images/13-pull-requests/overview/01-overview.png)

You *must* ask to have the files on *your* branch merged into another branch, and this requires opening a new **Pull Request** (PR). A pull request is a request to approve merging the contents of one branch into another. For example, an author might work on their own **Authoring branch** by adding new images into a lesson. By opening a new pull request, the author can ask another contributor (like a reviewer) to evaluate the new images *before* the images are added back into the **master branch** on GitHub or Azure DevOps.

> **Note**: Read more about GitHub PRs on the page [About pull requests](https://help.github.com/en/github/collaborating-with-issues-and-pull-requests/about-pull-requests). To create a new pull request, follow the guide [Create pull request]({{site.baseurl}}/pull-requests/create-pr.html).

{% include appendices.html %}

{% include paginator.html %}
