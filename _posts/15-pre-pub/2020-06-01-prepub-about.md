---
layout: page
title: About prepublication
subtitle:
description: A guide to the prepublication preparations section of this website
author: mkavana
date: 01 Jun 2020
post-number: 15.1
category: pre-pub
position-in-category: 1
include-in-pre-reqs: "false"
include-in-quickstart: "false"
video_url: "none"
---

This guide provides an overview of the prepublication preparations for a typical project, and describes the remaining guides in the **Prepublication preparations** section of this website.

> **Note**: The prepublication preparations section is *only* relevant to projects that have a requirement to convert finalized Markdown files (**\.md**) into Microsoft Word documents (**\.docx**) using Pandoc. The prepublication guides *do not* describe creating or editing PowerPoint presentation files (\.ppt), or other supporting resources.
>
> Requirements vary between projects, adapt the prepublication preparation guides to suit the particular requirements for the project you are working on. If you're unsure about your project's requirements, ask your project manager for help.
>

## Topics in this guide

- [Topic 1: An overview of prepublication preparations](#topic1)

{% include video.html %}

## Topic 1: An overview of prepublication preparations {#topic1}

Where relevant, the file conversion process involves creating a Microsoft Word document from each markdown file that has passed all reviewing, editing, and testing stages. Typically, finalized markdown files are stored in a designated directory (for example, on GitHub, Azure DevOps, Teams, or SharePoint). The file conversion process is usually performed by a dedicated WayPoint team member who is responsible for making the prepublication preparations.

> **Note**: The designated directory for storing finalized markdown files varies between projects. Ask your project manager where the finalized markdown files are stored for the project you're working on, and how to access them. Your project manager can also identify the WayPoint team member responsible for making prepublication preparations.
>

### Required file conversion tools

Markdown files (**\.md**) are converted into Microsoft Word documents (**\.docx**) using *Pandoc*. Pandoc is a free and open-source software program for converting documents. The conversion process also uses a set of *file conversion tools* from the zip archive **conversion_tools \.zip**. The zip archive contains the following file conversion tools:

- *reference \.dotx*. During the file conversion process, Pandoc reads the text formatting and styles defined in **reference \.dotx**, and applies them to the Word Documents it creates. For example, for all occurrences of the **Heading 1 markdown element** in a markdown file, like `# Example heading 1`, Pandoc applies the **Heading 1 style** defined in **reference \.dotx** to the corresponding Word Document it creates.

- *convert_md_to_docx \.bat*. In a single operation, the batch script file **convert_md_to_docx \.bat** converts all the markdown files in a directory into Word documents. The batch script uses Pandoc to apply the text formatting and styles defined in **reference \.dotx**. To work correctly, both **convert_md_to_docx \.bat** and **reference \.dotx** *must* be in the same directory when you run the batch script.

- *template \.dotx*. After Pandoc creates a Word document, the contents of the document *must* be styled using a template file, like **template \.dotx**. The template file is "attached" to a converted Word document, and styles from the template are applied to the document's contents in Word "manually".

### Prepublication preparation guides

The following are descriptions of the remaining guides in the **Prepublication preparations** section of this website.

- [Setup file conversion tools]({{site.baseurl}}/pre-pub/setup-tools.html) describes how to set up Pandoc, and the file conversion software tools in **conversion_tools \.zip**.

- [Convert markdown to doc]({{site.baseurl}}/pre-pub/pdoc-convert.html) describes how to use the batch script **convert_md_to_docx \.bat**, and reference file **reference \.dotx**, to convert the markdown files in a directory to Microsoft Word documents.

- [Style a doc in Word]({{site.baseul}}/pre-pub/style-doc.html) describes how to attach the template file **style_template \.dotx**, and use it to style the contents of a converted document, with Microsoft Word.

{% include appendices.html %}

{% include paginator.html %}
