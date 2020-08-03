---
layout: page
title: Configure styles in Word
subtitle:
description:
author:
date: 01 Jun 2020
post-number: 15.4
category: pre-pub
position-in-category: 4
include-in-pre-reqs: "false"
include-in-quickstart: "false"
video_url: "none"
---

This guide describes how to attach the style template file **template \.dotx** to a Microsoft Word document, and apply styles from the template to the document's contents in Microsoft Word.

> **Note**: As an example, the guide uses **template \.dotx** downloaded by following the guide [Setup file conversion tools]({{site.baseurl}}/pre-pub/setup-tools.html). Replace **template \.dotx** with the correct style template file for the course you're working on. Ask your project manager about the correct style template file for your project, and how to access it.
>
> Typically, only the styles **Heading 1**, **2**, **3**, **4**, **5**, and **Hyperlink** are applied by Pandoc during conversion. For all other text content, Pandoc applies the style **Normal/ Paragraph normal**. So, some content must be styled "manually" in Microsoft Word.
>

<!-- {% include prerequisites.html %} -->

## Topics in this guide

- [Attach the style template file in Microsoft Word](#attach-dotx)
- [Configure style options in Microsoft Word](#configure-dotx)

{% include video.html %}

## Attach the style template file in Microsoft Word {#-attach-dotx}

Complete the following steps to attach the style template file **template \.dotx** to a Word document converted from markdown.

1. In Microsoft Word, open the document you want to apply styling to.

2. Go to **File** > **Options**, and in the **Word Options** dialogue box, choose **Add-ins**.

3. In the dropdown box **Manage:**, select **Templates**, and then choose **Go**.

    ![The 'Word Options' dialogue box in Microsoft Word](../assets/images/15-pre-pub/config-styles/attach-template-003.png)

4. The **Templates and Add-ins** dialogue appears.

    In the **Templates and Add-ins** dialogue, select **Attach**, and locate the file **template \.dotx** you downloaded in previous guide [Setup file conversion tools]({{site.baseurl}}/pre-pub/setup-tools.html).

    Check the option to **Automatically update document styles**, then select **OK**.

    ![The 'Templates and Add-ins' dialogue box in Microsoft Word](../assets/images/15-pre-pub/config-styles/attach-template-004.png)

    > **Note**: Keep the document open to follow the steps in [Configure style options in Microsoft Word](#configure-dotx).
    >

You've attached **template \.dotx** to a Word document successfully.

## Configure style options in Microsoft Word {#configure-dotx}

Complete the following steps to configure the style options in Microsoft Word.

1. In Microsoft Word, open a document you want to apply styling to, and attach **template \.dotx** by following the steps in [Attach the style template file in Microsoft Word](#attach-dotx).

2. Open the **Styles** pane with the shortcut keys **Ctrl** + **Shift** + **Alt** + **S**, or by using the **Expand window** icon below the **Style** mini toolbar.

    ![Options for opening the 'Styles' panel in Microsoft Word](../assets/images/15-pre-pub/config-styles/restrict-styles-002.png)

3. In the **Styles** pane, select the button **Manage styles**.

    ![The 'Styles' panel in Microsoft Word](../assets/images/15-pre-pub/config-styles/restrict-styles-003.png)

4. In the **Manage Styles** dialogue, go to the **Restrict** tab

    Enable the option to **Limit formatting to permitting styles**, then select **OK**.

    ![The 'Manage Styles' dialogue box in Microsoft Word](../assets/images/15-pre-pub/config-styles/restrict-styles-004.png)

5. Return to the **Styles** pane, and then select **Options**.

    In the **Style Pane Options** dialogue, set the dropdown **Select styles to show:** to **In current document**, and then choose **OK**.

    ![The 'Style Pane Options' dialogue box in Microsoft Word](../assets/images/15-pre-pub/config-styles/restrict-styles-005.png)

You've configured the style options in Microsoft Word successfully.

{% include appendices.html %}

{% include paginator.html %}
