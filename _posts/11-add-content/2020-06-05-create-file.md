---
layout: page
title: Create new markdown file in VSC
subtitle:
description:
author:
date: 01 Jun 2020
post-number: 11.5
category: add-content
position-in-category: 5
include-in-pre-reqs: "false"
include-in-quickstart: "false"
video_url: "none"
---

This guide describes how to create a new markdown file using the Visual Studio Code editor (VSC).

{% include prerequisites.html %}

## Topics in this guide

- [Create a new markdown file using VSC](#new-markdown-file)

{% include video.html %}

## Create a new markdown file using VSC {#new-markdown-file}

Complete the following steps to create a new markdown file using VSC.

1. Open VSC, and choose **File** > **Open folder** from the top menu.

    !['Open folder' file menu in VSC](../assets/images/11-add-content/new-file/create-new-001.png)

2. Use the **VSC open folder** file explorer to select the local repo folder on your computer, then choose **Select folder**.

    For example, in the following image, the local repo folder named **docs-v2-DEV** is selected.

    !['Select folder' option in the 'VSC open folder' file explorer](../assets/images/11-add-content/new-file/create-new-002.png)

3. Use the **VSC explorer** (on the left) to go to the folder that will contain your new markdown file.

    For example, in the following image, the folder named **11-add-content** is selected in the **VSC explorer**.

    ![Example folder in VSC explorer](../assets/images/11-add-content/new-file/create-new-003.png)

    > **Note**: The **VSC status bar**, at the bottom of the editor window, indicates the name of the branch that VSC is currently switched to. For example, in the previous image, the **VSC status bar** indicates that VSC is currently switched to the branch named **update-add_content-section**. To avoid overwriting your files, switch VSC to the correct branch by following the guide [Switch branches]({{site.baseurl}}/branches/switch-branch.html).
    >

4. Right select the folder that will contain your new markdown file, and choose **New file** from the VSC **File menu**.

    !['New file' option selected from the 'File menu' in VSC](../assets/images/11-add-content/new-file/create-new-004.png)

5. Enter a name for the new file in the **text box** provided, followed by the markdown file extension **\. md**.

    For example, in the following image, the new filename **2020-06-05-author-outline\. md** is entered in the **text box**.

    ![Example file name entered in the 'new file name text box'](../assets/images/11-add-content/new-file/create-new-005.png)

6. VSC will open your new markdown file in an **editor tab** (on the right), and switch focus to the new tab.

    For example, in the following image, the new markdown file named **2020-06-05-author-outline\. md** is open in the **editor tab** (on the right).

    ![Example file open in a VSC editor tab](../assets/images/11-add-content/new-file/create-new-006.png)

7. Add content to the new file by following the guide [Add/ edit markdown in VSC]({{site.baseurl}}/add-content/edit-in-vsc.html).

    For example, in the previous image, a level 1 heading, a level 2 heading, and a paragraph with placeholder text have been added into the markdown file in the **VSC editor tab**.

You created a new markdown file using VSC successfully.

{% include appendices.html %}

{% include paginator.html %}
