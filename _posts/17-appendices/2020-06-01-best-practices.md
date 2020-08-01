---
layout: page
title: Best practices guide
subtitle: Appendix A
description: Best practices guidelines
author: mkavana
date: 01 Jun 2020
post-number: 17.1
category: appendices
position-in-category: 1
include-in-pre-reqs: "false"
include-in-quickstart: "false"
video_url: "none"
---

The following topics provide best practice guidelines to help you develop, review, edit, and prepare course content.

- [Topic 1: Set the correct Git credentials](#topic1)
- [Topic 2: Get the latest files from GitHub or Azure DevOps](#topic2)
- [Topic 3: Stage, commit, and push regularly](#topic3)
- [Topic 4: Backup your work](#topic4)
- [Topic 5: Use a clean repo](#topic5)
- [Topic 6: Rollback files in a GitHub repo](#topic6)
- [Topic 7: Do not copy and paste characters into markdown files](#topic7)
- [Topic 8: Do not use HTML inside markdown files](#topic8)

## Topic 1: Set the correct Git credentials {#topic1}

Ensure you've set the correct Git credentials by following the guide [Set Git credentials]({{site.baseurl}}/install/set-git-credentials.html).

Complete the following steps to edit your existing Git credentials in Visual Studio Code (VSC):

- Open VSC
- Select **Terminal** > **New Terminal**
- Type the command `git config`, and press **Enter**
- Edit and save your Git credentials

## Topic 2: Get the latest files from GitHub or Azure DevOps {#topic2}

Before you make changes to the files in your local repository (repo), get the latest files from the project's remote repo on GitHub or Azure DevOps using `git pull`. Use `git pull` by following the guide [Update branch]({{site.baseurl}}/branches/pull-updates.html), or by completing the following steps:

- Open VSC
- Select **Terminal** > **New Terminal**
- Type `git pull`, and press **Enter**

Use the **VSC Terminal** to perform `git pull` actions. Running `git pull` from the **VSC Command Palette** will not always update the files in your local repo correctly.

## Topic 3: Stage, commit, and push regularly {#topic3}

Stage, commit, and push the changes you make as regularly as possible. At the end of each day, and during each day, stage, commit, and push any changes you make to the files in your local "up" to GitHub or Azure DevOps. Regularly staging, committing, and pushing can mitigate against common problems, such as:

- Loosing work due to disk failure
- Forgetting which files you changed and saved
- Wasting time reassessing the work you did
- Merge conflicts

> **Note**: Save, stage, commit, and push your file changes by following the guide [Send (push) files]({{site.baseurl}}/branches/push-files.html).
>

## Topic 4: Backup your work {#topic4}

Create backups of your work periodically. To create a backup:

- Copy the entire contents of your local repo folder
- Paste the contents into a backup folder on your computer

Make a backup at the end of each day, especially at the end of a particularly productive day.

## Topic 5: Use a clean repo {#topic5}

Ensure you've a "clean" local repo before you start working on files. This is particularly important if you're unsure about which files you updated, or the state of your local repo. Before you update files, complete the following steps to create a clean repo:

- Pull the latest files from the project's remote repo (on GitHub or Azure DevOps) by following the guide [Update branch]({{site.baseurl}}/branches/pull-updates.html)
- Copy the contents of your local repo, and paste them into your backup folder
- Delete your original local repo (*do not delete* the backup copy you just made)
- Make a new clone of the project's remote repo using `git clone` by following the guide [Download course files (clone repo)]({{site.baseurl}}/download-files/clone-repo.html).

Adopting this approach will get the latest files from GitHub or Azure DevOps, in a clean state, into your local repo. Your local repo will be up-to-date with GitHub or Azure DevOps. This means you don't need to worry about using obsolete files, push errors, or merge conflicts. If you haven't accessed files in your local repo (or branch) for some time, this approach provides a "quick and easy" way to create a clean working environment.

## Topic 6: Rollback files in a GitHub repo {#topic6}

Revert to an earlier version of a file, or repo state, if you need to. On GitHub, you can view a file's history and revert (or rollback) a file to a previous version. Only consider reverting to a previous file version when you need to retrieve a file's contents.

To rollback a file on GitHub:

- Sign in to GitHub
- Select the file you want to rollback
- Choose **History**
- Select the button **retrieve**
- Choose the version of the file you want to revert to

## Topic 7: Do not copy and paste characters into markdown files {#topic7}

Adhere to using the VSC default character set. **Do not copy and paste characters into markdown files** that aren't in the VSC default character set. Copying and pasting characters into markdown files can cause issues that may not be immediately apparent.

Some characters in VSC are different to those used in Microsoft Word, including:

- Apostrophes
- Double and single quotation marks
- Bullet points

Contributors, and reviewers in particular, *must not* attempt to correct character styles by copying and pasting characters into markdown files. The correct character styles will be added later in the process.

> **Note**: For more information about writing in Markdown, refer to the guide [Markdown syntax guide]({{site.baseurl}}/add-content/syntax.html). For more information about adding markdown into a file in VSC, refer to the guide [Add/ edit markdown in VSC]({{site.baseurl}}/add-content/edit-in-vsc.html).
>

## Topic 8: Do not use HTML inside markdown files {#topic8}

Refrain from using HTML inside markdown files. Adding HTML to markdown files can cause rendering issues that may not be obvious in VSC, on GitHub, or Azure DevOps. The following HTML element tags are particularly problematic, and should not be used inside markdown files:

- HTML line break element tag `<br>`
- HTML horizontal line element tag `<hr>`
- HTML paragraph element tags `<p> <\p>`
- HTML image element tags `<img> <\img>`

> **Note**: For more information about writing in Markdown, refer to the guide [Markdown syntax guide]({{site.baseurl}}/add-content/syntax.html). For more information about adding markdown into a file in VSC, refer to the guide [Add/ edit markdown in VSC]({{site.baseurl}}/add-content/edit-in-vsc.html).
>

{% include paginator.html %}
