---
layout: page
title: Setup file conversion tools
subtitle:
description:
author:
date: 01 Jun 2020
post-number: 15.2
category: pre-pub
position-in-category: 2
include-in-pre-reqs: "false"
include-in-quickstart: "false"
include-in-azdevops-quickstart: "false"
video_url: "none"
---

This guide describes how to download and install Pandoc, and setup additional software tools for converting Markdown files (**\.md**) into Microsoft Word documents (**\.docx**).

## Topics in this guide

- [Download and install Pandoc](#pandoc-install)
- [Download and extract file conversion tools](#convert-tools)

{% include video.html %}

## Download and install Pandoc {#pandoc-install}

Complete the following steps to download and install Pandoc on your computer.

1. Open a web browser, and go to the webpage [Download Pandoc](https://pandoc.org/installing.html).

2. If you use the Windows operating system (64-bit version), select **Download the latest installer for Windows (64-bit)**.

    Download and save the **Pandoc installer file** to a suitable location on your computer.
  
    > **Note**: If you do not use Windows 64-bit, choose your operating system platform (like Linux or macOS, etc.) from the menu on the right side. Follow the online instructions for accessing the Pandoc **Download page** to download and install the version of Pandoc appropriate to your operating system.
    >

    ![The download Pandoc webpage](../assets/images/15-pre-pub/setup/pdoc-install-002.png)

3. When the **Pandoc installer file** has downloaded, go to the location where you saved the installer file, and run the file.

    > **Note**: At the time of writing, Pandoc 2.9 is the latest version. Adapt the steps to suit the version of Pandoc you're installing.
    >

4. Use the checkbox **I accept the terms in the Licence Agreement** to accept the terms of the Pandoc licence agreement, then select **Install**.
  
    > **Note**: If you prefer, allow Pandoc to be used by all users of your computer by enabling the checkbox option to **Install for all users of this machine**.
    >

    ![The Pandoc installer licence agreement checkbox](../assets/images/15-pre-pub/setup/pdoc-install-004.png)

5. When the installation has completed, choose **Finish**.

    ![Pandoc installation completed message](../assets/images/15-pre-pub/setup/pdoc-install-005.png)

    > **Note** Pandoc does not provide a *Graphical User Interface* (GUI). Instead, Pandoc provides a Command Line Interface (CLI) to perform file conversions in a Shell (like Windows Command Prompt, or Terminal in Linux and macOS).
    >

You've downloaded and installed Pandoc successfully.

> **Note**: For more information about using Pandoc, refer to the Pandoc documentation guide [Getting started with pandoc](https://pandoc.org/getting-started.html).
>

## Download and extract file conversion tools {#convert-tools}

Complete the following steps to download and extract additional software tools for converting markdown files into Word documents.

> **Note**: The additional file conversion software tools are compressed in the zip file **conversion_tools \.zip**, and stored on GitHub.

1. Select [Download conversion tools]({{site.baseurl}}/assets/download/conversion_tools.zip), and save the file **conversion_tools \.zip** to a suitable location on your computer.

    > **Note**: If the download link doesn't work, open a web browser, sign to GitHub, and select the download link again.
    >

2. When **conversion_tools \.zip** has downloaded, go to the location where you saved the file, and extract the contents.

    > **Note**: If don't have software to extract the zip file, download and install software like [7-zip](https://www.7-zip.org/) or [WinZip](https://www.winzip.com/).
    >

3. Extracting the zip file's contents creates the directory **conversion_tools**.

    Confirm that the directory **conversion_tools** contains the following files:

    - reference \.dotx
    - convert_md_to_docx \.bat
    - template \.dotx

    ![The directory 'conversion_tools' with three extracted files](../assets/images/15-pre-pub/setup/tools-zip-003.png)

You have downloaded and extracted **conversion_tools \.zip** successfully.

{% include appendices.html %}

{% include paginator.html %}
