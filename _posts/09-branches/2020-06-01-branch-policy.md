---
layout: page
title: Project branching policies
subtitle:
description: A guide to the branching policies that apply to a typical project
author: mkavana
date: 01 Jun 2020
post-number: 9.1
category: branches
position-in-category: 1
include-in-pre-reqs: "false"
include-in-quickstart: "false"
video_url: "none"
---

This guide describes the branching policies that apply to a typical project.

{% include prerequisites.html %}

## Topics in this guide

- [Protected branches](#protected-branch)

{% include video.html %}

## Protected branches {#protected-branch}

Git administrators often implement (branching) policies to protect the contents of certain branches from being overwritten. For example, you may not be able to apply edits directly to the **master** branch for the project you're working.

Typical requirements for making changes to a protected branch include the following:

- contributors cannot apply changes to a protected branch directly
- contributors can only apply changes to a protected branch by merging changes from another branch (*compare* branch)
- a pull request is required to merge a compare branch into a protected branch
- all changes proposed on a compare branch must be approved by a reviewer before they can be merged
- merging is restricted to the repository administrators (or similar role)

Branches can be protected in different ways, like by role, and branching policies can vary between projects. Ask your project manager about the particular branching policies that apply to the project you're working on.

> **Note**: The branching structures that apply to the different roles in a typical project are described in the guide [General project workflow]({{site.baseurl}}/workflow/general-workflow.html). For more information about branching policies, refer to [About protected branches](https://docs.github.com/github/administering-a-repository/about-protected-branches].

{% include appendices.html %}

{% include paginator.html %}
