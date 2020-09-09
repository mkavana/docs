---
layout: multi
title: Download course files (clone repo)
subtitle: GitHub
description: A guide to cloning a project's GitHub repository
author: mkavana
date: 01 Jun 2020
post-number: 7.3
category: download-files
position-in-category: 3
include-in-pre-reqs: "true"
include-in-quickstart: "true"
include-in-azdevops-quickstart: "false"
video_url: "none"
---

In this guide, you will download (or clone) a copy of the course files from GitHub to your computer.

{% include prerequisites.html %}

## Topics in this guide

- [Clone the GitHub repo](#clone-github)

{% include video.html %}

## Clone the GitHub repo {#clone-github}

Complete the following steps to download (**clone**) the project's repo from GitHub.

1. Open a web browser. Go to [https://github.com](https://github.com), and sign into GitHub.

2. Go to the project's GitHub repo at `https://github.com/WaypointVentures/<project repo name>`, where `<project repo name>` refers to the name of the project you are working on.

    For example, for the "Az Funds" project, go to [https://github.com/WaypointVentures/azfundedu](https://github.com/WaypointVentures/azfundedu).

3. Use the dropdown to choose the **master** branch, then select the green **Clone or download** button. Copy the GitHub clone URL by using the copy icon beside the URL, as shown in the following image.

    ![github repo clone or download url pane](../assets/images/07-download-files/clone/github/git-clone-repo-003.png)

4. On your computer, open **VSC** and go to **View** > **Command Palette**. Type **git clone** into the dialogue box.

    ![git clone command search](../assets/images/07-download-files/clone/github/git-clone-repo-004.png)

    > **Note**: You can run other Git commands within the VSC command palette. Not all Git commands are available from the VSC command palette. Use the VSC Terminal to access more Git commands.
    >
    > The subset of Git commands available from the VSC command palette should be sufficient for the current project. For help with scenarios not covered by the VSC command palette, ask your project manager.

5. Select the `git clone` command from the list. In the **Repository URL** dialogue, paste in the GitHub clone URL you copied previously, then press **Enter**.

    ![git clone command git url](../assets/images/07-download-files/clone/github/git-clone-repo-005.png)

6. A **Select Folder** window will appear. Inside the **Select Folder** window, set a location on your computer where you want to save your copy of the GitHub repo, then choose **Select Repository Location**.

    Save a copy of the GitHub repo wherever you prefer.

    > **Note**: Saving the GitHub repo to remote storage, such as OneDrive, is not recommended. Remote storage typically uses longer file paths, which may cause problems. Clone the GitHub repo to local storage (i.e. on your computer) instead.

    ![select repository location dialogue](../assets/images/07-download-files/clone/github/git-clone-repo-006.png)

7. A progress indicator will appear in the bottom left corner of VSC. When it finishes VSC will prompt you to open the repo you cloned.

    ![git clone status prompt](../assets/images/07-download-files/clone/github/git-clone-repo-007a.png)

    ![git clone open prompt](../assets/images/07-download-files/clone/github/git-clone-repo-007b.png)

8. Choose **Open**. The (locally) cloned repo will open in **VSC** on the **master** branch.

    You can reopen the local repo at anytime in VSC using **File** > **Open Folder...**. The local repo will be displayed in the VSC folder view (side bar).

    > **Note**: A copy of the files and folders from GitHub are now present on your computer. Your copy is an exact match of the GitHub repo.

You have cloned the GitHub repo successfully!

{% include appendices.html %}

{% include paginator.html %}
