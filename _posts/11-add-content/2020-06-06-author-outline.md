---
layout: page
title: Use author outlines
subtitle:
description: A guide to using author outlines create content in markdown with VSC
author:
date: 01 Jun 2020
post-number: 11.6
category: add-content
position-in-category: 6
include-in-pre-reqs: "false"
include-in-quickstart: "false"
video_url: "none"
---

This guide describes how to use author outlines to create content in markdown with the Visual Studio Code editor (VSC).

{% include prerequisites.html %}

## Topics in this guide

- [Topic 1: An overview of author outlines](#topic1)
- [Topic 2: Use a markdown element from an author outline](#topic2)

{% include video.html %}

## Topic 1: An overview of author outlines {#topic1}

This topic describes what author outlines are, why they are used, and how to access them.

### What author outlines are

Some project's have **author outlines** available for you to use. An author outline is a markdown file that contains markdown elements, like tables or multilevel lists. You can copy the markdown elements from an author outline and paste them into your markdown file to create content quickly.

> **Note**: Ask your project manager if there are author outlines available for the course you are working on, and where to find them.

In the following image, a portion of content from a typical author outline is open in VSC.

![Portion of content from an example author outline](../assets/images/11-add-content/outlines/sample-001.png)

### Why author outlines are used

Author outlines are used to provide the following:

- a framework for authoring content in each deliverable file
- an outline of the elements required in each deliverable file
- comments on authoring various markdown elements, with guidelines and suggestions
- guidance with markdown syntax, document formatting and structural requirements
- reusable boilerplate text for authors to copy and paste

### How to access author outlines

Depending on the project you are working on, author outlines can be made available for use in different ways. For example, author outlines can be stored:

- within the project's remote repository (repo), inside the folders for each module or in a designated folder elsewhere in the repo.
- outside the project's remote repo, like on SharePoint.

> **Note**: Ask your project manager if there are author outlines available for the course you are working on, and where to find them.

As an example, the following image lists the author outlines for the course **40574A Azure Fundamentals** ("Az Funds"), from the project's GitHub repo.

![List of example author outlines for the 'Az Funds' course on GitHub](../assets/images/11-add-content/outlines/sample-002.png)

> **Note**: The previous list of author outlines for the "Az Funds" course are *course component specific*. For example, there are separate author outlines for the **Learning activity**, **Student guide**, and **Lesson plan**. The author outlines are stored in the project's GitHub repo inside the designated folder **azfundedu/Author templates and outlines/Final/md/**.
>
> Where relevant, a list of deliverables and author outlines is available from the **Bill of Materials** (BOM) for course you are working on. Direct all your BOM related queries to your project manager.
>

## Topic 2: Use a markdown element from an author outline {#topic2}

Complete the following steps to copy a markdown element from an author outline on GitHub, and paste the element into a markdown file in VSC.

> **Note**: As an example of a markdown element, this guide uses an **Exam objectives table** from an author outline in the WayPoint Ventures' test repo (**Testrepo1**) on GitHub. Modify the following instructions to suit your preferred markdown element, author outline, and remote repo.
>

1. In a web browser, go to the URL for **Testrepo1** on GitHub at [https://github.com/WaypointVentures/Testrepo1/](https://github.com/WaypointVentures/Testrepo1/).

2. Sign into GitHub, and go to the repo's designated **author outline storage folder** on the path **Testrepo1/Author templates and outlines/Final/md/**

    ![Example of a designated 'author outline storage folder' on GitHub](../assets/images/11-add-content/outlines/use-outline-002.png)

3. Select the author outline **Lesson Plan outline\. md**.

    ![Example 'author outline' selected on GitHub](../assets/images/11-add-content/outlines/use-outline-003.png)

4. Choose the **Raw** button to access an unparsed ("raw") markdown version of the author outline.

    !['Raw' button on GitHub](../assets/images/11-add-content/outlines/use-outline-004.png)

5. Scroll down through the author outline's contents, and locate the markdown element **Exam objectives table** (just below the level 1 heading **# Objectives**).

    !['Exam objectives table' inside an example author outline on GitHub](../assets/images/11-add-content/outlines/use-outline-005.png)

6. Select the table contents from the **beginning of the first row**, to the **end of the caption**, then copy the table to your clipboard (use the shortcut keys **CTRL** + **C** to copy or **right select** the table, then choose **copy**).

    !['Exam objectives table' selected from inside an example author outline on GitHub](../assets/images/11-add-content/outlines/use-outline-006.png)

7. Open VSC, and choose **File** > **Open folder** from the top menu.

    !['Open folder' file menu in VSC](../assets/images/11-add-content/outlines/use-outline-007.png)

8. Use the **VSC open folder** file explorer to select the local repo folder on your computer, then choose **Select folder**.

    For example, in the following image, the local repo folder named **test-repo** is selected.

    !['Select folder' option in the 'VSC open folder' file explorer](../assets/images/11-add-content/outlines/use-outline-008.png)

9. Use the **VSC explorer** (on the left) to go to the folder that contains the markdown file you want to paste the table into.

    For example, in the following image, the folder named **Module-02** is selected in the **VSC explorer**.

    ![Example folder in VSC explorer](../assets/images/11-add-content/outlines/use-outline-009.png)

    > **Note**: The **VSC status bar**, at the bottom of the editor window, indicates the name of the branch that VSC is currently switched to. For example, in the previous image, the **VSC status bar** indicates that VSC is currently switched to the branch named **master**. To avoid overwriting your files, switch VSC to the correct branch by following the guide [Switch branches]({{site.baseurl}}/branches/switch-branch.html).
    >

10. In the **VSC explorer** (on the left), select a markdown file to paste the table into.

    For example, in the following image, the markdown file named **Mod-02-Example_file \.md** is selected.

    ![Example markdown file selected in 'VSC explorer'](../assets/images/11-add-content/outlines/use-outline-010.png)

11. In the **VSC editor tab** (on the right), find an appropriate place inside the markdown file, and paste in the **Exam objectives table** that you copied from the author outline in **Step 6**.

    For example, in the following image, the **Exam objectives table** is pasted below the heading **Module 02 test file**.

    !['Exam objectives table' pasted into an example markdown file](../assets/images/11-add-content/outlines/use-outline-011.png)

12. In the **VSC editor tab** (on the right), modify the contents of the **Exam objectives table** to suit your requirements.

    For example, in the following image, the markdown comments are removed from around the **Exam objectives table**, and text is added into the table cells.

    !['Exam objectives table' with markdown comments removed and text added to the table cells, inside an example markdown file](../assets/images/11-add-content/outlines/use-outline-012.png)

13. To complete adding content to the markdown file, go to **Step 5** of the guide [Add/ edit markdown in VSC]({{site.baseurl}}/add-content/edit-in-vsc.html).

You have copied and pasted a markdown element from an author outline on GitHub into a markdown file in VSC successfully.

> **Note**: As explained in [Topic 1: An overview of author outlines](#topic1), author outlines can be stored inside or outside a project's remote repo. To use a markdown element from an author outline that's *not* on GitHub, complete the following:
>
> - Download the author outline from the designated **author outline storage location** to your computer. For example, download an author outline from SharePoint.
> - Open the author outline you downloaded. For example, open the author outline in VSC.
> - In the author outline file, locate and copy the required markdown element. For example, copy the **Exam objectives table**.
> - Paste the element into the markdown file you are working on.
> - If necessary, edit the element you pasted inside the markdown file. For example, remove markdown comments and update any placeholder text to match the requirements for the file you are working on (like course code or module number).
>

{% include appendices.html %}

{% include paginator.html %}
