---
layout: multi
title: View course files in web browser
subtitle: AzDevOps
description: A guide to viewing an AzDevOps repo in a web browser.
author: mkavana
date: 01 Jun 2020
post-number: 7.1
#category: download-files
#position-in-category: 1
include-in-pre-reqs: "false"
include-in-quickstart: "false"
video_url: "none"
---

In this guide you'll view the course files on AzDevOps using a web browser.

Using a browser provides a "quick and easy" way to view course files without installing or configuring additional software tools. For example, as part of a content review, if you don't need to add comments or make edits to the content, use this guide.

> **Note**: The procedure for downloading files for *editing* with Visual Studio Code (VSC) is described in the guide [Download course files]({{site.baseurl}}/download-files/clone-repo.html).
>

{% include prerequisites.html %}

## Topics in this guide

- [Locate the course files on AzDevOps](#locate-azdevops)
- [View the course files on AzDevOps](#view-azdevops)

{% include video.html %}

## Locate the course files on AzDevOps {#locate-azdevops}

The course files for each AzDevOps project are stored in a dedicated AzDevOps repository (remote repo). Ask your project manager for the URL (link) to the project's remote repo.

A project's remote repo can contain different versions of the course files. Within the repo, each set (or version) of the files is stored in a compartment called a **branch**. To choose the branch with the version of the files you want to view, complete the steps in the following topic [View the course files on AzDevOps](#view-azdevops).

## View the course files on AzDevOps {#view-azdevops}

The following steps demonstrate how to view the contents of an AzDevOps repo in a web browser, and how to access the branch with the files you require.

1. Open a web browser, go to the AzDevOps website at [https://dev.azure.com](https://dev.azure.com), and sign in.

2. On the projects tab, locate the project you require, and select the **Repos** icon.

    For example, in the following image, the **Repos** icon for the project **example-repo** is selected.

    ![Example AzDevOps repo project with the 'Repos' icon selected](../assets/images/07-download-files/browser/azdev/az-browser-view-002.png)

3. The **branch dropdown** indicates which branch AzDevOps is currently set to.

    For example, in the following image, the branch dropdown indicates that AzDevOps is set to the branch named **master**.

    ![Example AzDevOps repo with the 'branch dropdown' set to the 'master' branch](../assets/images/07-download-files/browser/azdev/az-browser-view-003a.png)

    Use the **branch dropdown** to view a list of available branches, and then choose the branch with the files you want to view.

    For example, in the following image, the branch **example-branch-mkavana** is selected.

    ![Example AzDevOps repo with the 'branch dropdown' set to the branch 'example-branch-mkavana'](../assets/images/07-download-files/browser/azdev/az-browser-view-003b.png)

4. The AzDevOps repo uses a standard file and folder structure. To browse the repo's contents, select **Files**, and go to the folder or file you require.

    For example, in the following image, the file **sample-file \.md** is selected in the folder **sample-folder**.

    > **Note**: Use your web browser's address bar to get the URL for a file on AzDevOps. The URL contains the path to the file and the branch name. You can share the URL with other contributors if you need to. The top menu indicates the branch name, and the full filepath is shown alongside it.
    >
    > For example, in the following image, the branch is **example-branch-mkavana** and the filepath is **sample-folders\sample-file \.md**.
    >

    ![Example AzDevOps repo with branch name and filepath](../assets/images/07-download-files/browser/azdev/az-browser-view-004.png)

You've viewed the course files on AzDevOps using a web browser successfully.

> **Note**: You *can* edit the files on AzDevOps within your web browser. However, the preferred procedure for making changes to markdown files is described in the guide [Add/ edit markdown in VSC]({{site.baseurl}}/add-content/edit-in-vsc.html).
>

{% include appendices.html %}
