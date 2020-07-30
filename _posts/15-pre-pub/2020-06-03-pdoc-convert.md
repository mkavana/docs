---
layout: page
title: Convert markdown to doc
subtitle:
description:
author:
date: 01 Jun 2020
post-number: 15.3
category: pre-pub
position-in-category: 3
include-in-pre-reqs: "false"
include-in-quickstart: "false"
video_url: "none"
---

This guide describes how to use the software tools **convert_md_to_docx \.bat** and **reference \.dotx** to convert the markdown files (\.md) in a directory to Word documents (\.docx).

> **Note**: This guide assumes you've setup the required software tools by following the guide [Setup file conversion tools]({{site.baseurl}}/pre-pub/setup-tools.html). You *must* also have a copy of the markdown files you want to convert in a directory on your computer. Obtain a copy of the markdown files by cloning the project's remote repository (repo) on GitHub or Azure DevOps using the guide [Download course files (clone repo)]({{site.baseurl}}/download-files/clone-repo.html).
>
> Alternatively, if you don't want to clone the project's remote repo, you can download a zip file with the contents of a particular branch from GitHub. Sign in to GitHub, choose the branch with the markdown files you want to covert, select **Code**, and then choose the option to **Download ZIP**.
>
> For example, in the following image, the branch **edit-m02-l02** is selected in the GitHub repo **test-repo**, with the option to **Download ZIP**.
>
> ![Option to download a zip file from GitHub](../assets/images/15-pre-pub/convert/get-zip-001.png)
>
> As part of the conversion process, any images and graphics linked in the markdown file will be embedded into the converted Word documents. Before you begin converting files, copy the corresponding image and graphics directory (**media**) for the markdown files, and paste it into the markdown files directory, on correct file path (relative to the markdown files).
>

{% include prerequisites.html %}

## Topics in this guide

- [Topic 1: Convert markdown files to Word documents](#topic1)

{% include video.html %}

## Topic 1: Convert Markdown files to Word documents {#topic1}

Complete the following steps to use the software tools **convert_md_to_docx \.bat** and **reference \.dotx** to convert the markdown files in a directory to Word documents.

1. Go to the directory **conversion_tools** where you extracted the software tools **convert_md_to_docx \.bat** and **reference \.dotx** from the previous guide [Setup file conversion tools]({{site.baseurl}}/pre-pub/setup-tools.html).

2. Copy **convert_md_to_docx \.bat** and **reference \.dotx** to your clipboard.

    ![text](../assets/images/15-pre-pub/convert/pdoc-convert-002.png)

3. Go to the directory with the markdown files you want to convert, and paste **convert_md_to_docx \.bat** and **reference \.dotx** into the markdown files directory.

    ![text](../assets/images/15-pre-pub/convert/pdoc-convert-003.png)

    > **Note**: An alternative approach is to copy the markdown files and paste them into the directory **conversion_tools**.

4. Run the batch script file **convert_md_to_docx \.bat**.

    > **Note**: The batch script will open in a Shell, like Command Prompt. The batch script does not require interaction, and will close on completion.

5. When the batch script has finished, verify that the required number of Word documents were created.

    ![text](../assets/images/15-pre-pub/convert/pdoc-convert-005.png)

    > **Note**: When you've finished converting files, move the converted Word documents, the markdown files, and the software tools to an appropriate storage directory. To convert another set of markdown files, place them in a directory with software tools, and run **convert_md_to_docx \.bat** again.
   >

You've used the software tools **convert_md_to_docx \.bat** and **reference \.dotx** to convert markdown files in a directory to Word documents successfully.

{% include appendices.html %}

{% include paginator.html %}
