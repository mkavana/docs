---
layout: page
title: Fix linter issues
subtitle:
description: A guide to viewing and addressing markdown errors in VSC
author: mkavana
date: 01 Jun 2020
post-number: 11.7
category: add-content
position-in-category: 7
include-in-pre-reqs: "false"
include-in-quickstart: "false"
video_url: "https://web.microsoftstream.com/embed/video/6e3c80aa-76ee-46d1-81d8-55d7dadfd106?autoplay=false&amp;showinfo=true"
---

This guide describes how to view and address markdown errors in the Visual Studio Code editor (VSC).

The Microsoft [Docs Authoring Pack](https://marketplace.visualstudio.com/items?itemName=docsmsft.docs-authoring-pack) provides VSC extensions to check for markdown syntax errors (or "linting") and perform spelling checks. Addressing syntax and spelling errors helps to keep your markdown formatted correctly (or "clean"). Creating clean markdown can reduce the time that's required to edit your markdown later in the process.

> **Note**: The **Docs Authoring Pack** provides the following linting and spellchecking extensions:
>
> - [Docs linting](https://marketplace.visualstudio.com/items?itemName=docsmsft.docs-linting) provides linting that's specific to the markdown syntax used in Microsoft Docs articles.
> - [Markdown lint](https://marketplace.visualstudio.com/items?itemName=DavidAnson.vscode-markdownlint) is a general purpose markdown linter.
> - [Code spell checker](https://marketplace.visualstudio.com/items?itemName=streetsidesoftware.code-spell-checker) adds basic spellchecking functionality to VSC.
>

{% include prerequisites.html %}

## Topics in this guide

- [View syntax and spelling errors in VSC](#lint-view)
- [Address a syntax error in VSC](#error-syntax)
- [Address a spelling error in VSC](#error-spell)

{% include video.html %}

## View syntax and spelling errors in VSC {#lint-view}

Complete the following steps to view syntax and spelling errors in VSC.

1. In VSC, choose **File** > **Open**, from the top menu, and select a markdown file in your local repository (repo).

    For example, in the following image, the markdown file **Author quick start guide \.md** is open in the **VSC explorer panel**. The markdown file is in a local repo **Testrepo1**, cloned from the [WayPoint Ventures' test repository (**Testrepo1**) on GitHub](https://github.com/WaypointVentures/Testrepo1/).

    ![Example markdown file in the 'VSC explorer panel'](../assets/images/11-add-content/linter/lint-001.png)

    > **Note**: The **VSC status bar**, at the bottom of the editor window, indicates the name of the branch that VSC is currently switched to. For example, in the previous image, the **VSC status bar** indicates that VSC is currently switched to the branch named **master**. To avoid overwriting your files, switch VSC to the correct branch by following the guide [Switch branches]({{site.baseurl}}/branches/switch-branch.html).
    >

2. In the **VSC editor tab**, scroll through the markdown file to identify spelling and syntax errors. Spelling errors are underscored by a **blue colored line**, and syntax errors are underscored by a **yellow colored line**

    For example, in the following image, the markdown file open in the **VSC editor tab** contains three sets of **yellow colored lines** that indicate the following syntax errors:

   - On line number **12** an unnecessary space character is entered on a blank/ empty line.

   - The second-level bulleted list items on line numbers **18** to **22** are indented using too many space characters. There is also a missing blank/ empty line between the list item **- Task 1: Download and...** and the list item **- Visual Studio...**.

   - There is a missing blank/ empty line after the heading **## Appendices in this doc...** on line number **28**.

    ![Example of syntax problems in a markdown file detected by VSC](../assets/images/11-add-content/linter/lint-002.png)

    > **Note**: Apply different color themes to VSC until you find a theme that makes errors easier to detect. Find a new color theme in VSC by selecting **File** > **Preferences** > **Color Theme**, or with the shortcut keys **CTRL** + **T** + **CTRL** + **K**.
    >

3. For additional error details, open the VSC **PROBLEMS** panel by selecting the **problem icons** from the **VSC status bar**.

    ![VSC 'problems icons' in the VSC 'status bar'](../assets/images/11-add-content/linter/lint-003.png)

    > **Note**: The **VSC status bar** provides a separate count and icon for each type of problem it detects. VSC provides a count and icon for **Critical**, **Warnings**, and **Infos**. For example, in the previous image, there are **0 Critical**, **60 Warnings**, and **11 Infos** in the **VSC status bar**.
    >

4. In the VSC **PROBLEMS** panel, note the total number of problems, the list of error codes, the corresponding problem descriptions, and the line and character numbers where the problems occur.

    !['VSC problems panel' in the VSC editor](../assets/images/11-add-content/linter/lint-004a.png)

    For example, in the following image, the VSC **PROBLEMS** panel indicates there are **71** problems. One of the problems, a syntax error indicated by a **yellow colored alert icon** with error code **MD012**, is caused by **Multiple consecutive blank lines** on line number **464**. Another syntax error, with a **yellow colored alert icon**, concerns the language and region specific syntax **en-us** that's used in a hyperlink on line number **467**. The two spelling errors **familiarise** and **filess** are flagged with **blue colored information icons** on line numbers **264** and **338** respectively.

   ![Examples of syntax and spelling problems in the 'VSC problems panel'](../assets/images/11-add-content/linter/lint-004b.png)

5. Scroll through the list of problems in the VSC **PROBLEMS** panel for details about the remaining syntax and spelling errors.

    > **Note**: Keep the VSC **PROBLEMS** panel open to follow the steps in [Address a syntax error in VSC](#error-syntax).
    >

You have viewed syntax and spelling errors in VSC successfully.

## Address a syntax error in VSC {#error-syntax}

Complete the following steps to address a syntax error in VSC.

1. With the VSC **PROBLEMS** panel open, select a syntax error indicated with a **yellow colored alert icon** in the VSC **PROBLEMS** panel.

    For example, in the following image, the syntax error **MD009/no-trailing-spaces: Trailing spaces [Expected: 0 or 2; Actual: 1]** is selected. When the syntax error is selected from the VSC **PROBLEMS** panel, VSC focuses the VSC **Editor tab** on the line where the syntax error occurs in the markdown file. For example, the VSC **Editor tab** is focused on line number **462** in the following image.

    ![Example syntax error selected in the VSC 'Problems panel' and 'Editor tab'](../assets/images/11-add-content/linter/lint-fix-001.png)

2. In the VSC **Editor tab**, go to where the syntax error is flagged with a **yellow colored line**.

    For example, in the following image, the **yellow colored line** in the VSC **Editor tab** indicates an unnecessary trailing space character on line number **462**.

    ![Example syntax error on a line in the VSC 'Editor tab'](../assets/images/11-add-content/linter/lint-fix-002.png)

3. Address the syntax error by deleting the unnecessary space character.

    ![Example syntax error addressed in the VSC 'Editor tab' and 'Problems panel'](../assets/images/11-add-content/linter/lint-fix-003.png)

    > **Note**: In the previous image, after deleting the unnecessary space character, the **yellow colored line** is gone from the **Editor tab**. The syntax error is no longer listed in the VSC **PROBLEMS** panel. The total number of problems in the VSC **PROBLEMS** panel is decremented.
   >

4. Continue through the list of syntax errors in the **PROBLEMS** panel, and address each one.

    > **Note**: Address as many syntax errors as possible. Ignore certain syntax errors if you're intentionally using a markdown syntax that's different from what the linting tool expects. If you're unsure about a particular syntax error, ask your project manager for help.
    >
    > Keep the VSC **PROBLEMS** panel open to follow the steps in [Address a spelling error in VSC](#error-spell).
    >

You have addressed a syntax error in VSC successfully.

## Address a spelling error in VSC {#error-spell}

1. With the VSC **PROBLEMS** panel open, select a spelling error indicated with a **blue colored information icon** in the VSC **PROBLEMS** panel.

    For example, in the following image, the spelling error **"familiarise": Unknown word. cSpell [264, 169]** is selected in the VSC **PROBLEMS** panel. When the spelling error is selected from the VSC **PROBLEMS** panel, VSC focuses the VSC **Editor tab** on the line where the spelling error occurs in the markdown file. For example, the VSC **Editor tab** is focused on line number **264** in the following image.

    ![Example spelling error selected in the VSC 'Problems panel' and 'Editor tab'](../assets/images/11-add-content/linter/spell-fix-001.png)

2. In the VSC **Editor tab**, the spelling error is flagged with a **blue colored line**. **Right-select** the misspelled word in the VSC **Editor tab**, then choose the correct spelling from the list of suggestions.

    For example, in the following image, the correct US English language spelling for **familiarize** is selected in the VSC **Editor tab** on line number **464**.

    ![Correct spelling for a misspelled word selected in the VSC 'Editor tab'](../assets/images/11-add-content/linter/spell-fix-002a.png)

    > **Note**: Words that are not found in the spellchecker's dictionary are flagged as errors. To change the spellchecker's dictionary language, follow the instructions on page [Code spell checker](https://marketplace.visualstudio.com/items?itemName=streetsidesoftware.code-spell-checker). To add a (custom) word to the spellchecker's dictionary, **right-select** the flagged word in the VSC **PROBLEMS panel**, then choose **Add: "\<word\> to user dictionary**. All occurrences of the word will be removed from the list of spelling errors in the VSC **PROBLEMS panel**. For example, in the following image, the option is selected to **Add: "ptential" to user dictionary**.
    >
    > ![Option to add a word to the dictionary in a VSC 'Editor tab'](../assets/images/11-add-content/linter/spell-fix-002b.png)
    >

3. After a misspelled word is corrected (or added to the dictionary), the **blue colored line** is gone from the **Editor tab**. The spelling error is no longer listed in the VSC **PROBLEMS** panel. The total number of problems in the VSC **PROBLEMS** panel is decremented.

    For example, in the following image, the word **familiarise** is changed to **familiarize**.

    ![Example spelling error addressed in the VSC 'Editor tab' and 'Problems panel'](../assets/images/11-add-content/linter/spell-fix-003.png)

4. Continue through the list of spelling errors in the VSC **PROBLEMS** panel, and address each one.

    > **Note**: The spellcheck dictionary is not exhaustive. However, it can help you to identity and correct common spelling errors, and keep your markdown "clean".
    >

5. When you have addressed all linting and spellchecking errors, save, stage, commit, and push your markdown file to the project's remote repo on GitHub or Azure DevOps by following the guide [Send (push) files]({{site.baseurl}}/branches/push-files.html).

6. After you have pushed your markdown file to the project's remote repo, create a new pull request to merge the files by following the guide [Create pull request]({{site.baseurl}}/pull-requests/create-pr.html).

You have addressed a spelling error in VSC successfully.

{% include appendices.html %}

{% include paginator.html %}
