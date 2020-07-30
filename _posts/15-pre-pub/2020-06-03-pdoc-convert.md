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

This guide describes how to convert a Markdown file to a Word document.

{% include prerequisites.html %}

## Topics in this guide

- [Topic 1: D/L Files to convert?](#topic1)
- [Topic 3: Convert Markdown files to Word documents](#topic2)

{% include video.html %}

## Topic 1: D/L Files to convert? {#topic1}

## Topic 2: Convert Markdown files to Word documents {#topic2}

Complete the following steps to use the file **convert_to_DOCX.bat** to convert a Markdown file to a Word document.

The pandoc command is called from within the batch file `convert_to_DOCX.bat`. If we did not use the batch file we would need to convert each file individually from the command line.

1. Go to the folder in which you have the markdown files you wish to convert, in this example it is the module 5. The folder should also contain the following files, if not you need to obtain them as outlined in earlier tasks, otherwise the conversion process may fail.

    - `convert_to_DOCX.bat`
    - `reference.dotx`
    - `Academic ILT Courseware Template.dotx`
    - `media` folder (this contains the image files referenced in the markdown files)

    ![text](../assets/images/15-pre-pub/convert/pdoc-convert-001.png)

2. In File explorer, or whatever editor you are using, double click on the file `convert_to_DOCX.bat`. The batch will run, a command prompt window will open, it will not require any interaction, and it will close on completion.

3. Once the batch has file completed running, the folder should now contain a docx file for each .md file, as in the screenshot. In this case there are 12 docx files, your module may have more or less .md files, and this more or less .docx files.

    ![text](../assets/images/15-pre-pub/convert/pdoc-convert-003.png)

    > **Note**: Count the number of .md files and compare against the number of converted .docx files and ensure they match and that no files have been missed. If there has been accidental modification of the batch file, some of the path or file definitions could have changed which might affect the output. This is unlikely, but just do a count to make sure nothing has been missed.
    >

![text](../assets/images/15-pre-pub/convert/img-placeholder.png)

{% include appendices.html %}

{% include paginator.html %}
