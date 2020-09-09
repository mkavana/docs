---
layout: multi
title: Download course files (clone repo)
subtitle: AzDevOps
description: A guide to cloning an AzDevOps repo
author: mkavana
date: 01 Jun 2020
post-number: 7.3
#category: download-files
#position-in-category: 3
include-in-pre-reqs: "false"
include-in-quickstart: "false"
include-in-azdevops-quickstart: "true"
video_url: "none"
---

In this guide, you will download (or clone) a copy of the course files from AzDevOps onto your computer using the Visual Studio Code editor (VSC).

## Topics in this guide

- [Clone the AzDevOps repo](#clone-azdevops)

{% include video.html %}

## Clone the AzDevOps repo {#clone-azdevops}

Complete the following steps to clone the project's repository (repo) from AzDevOps using VSC.

1. Open a web browser, go to the AzDevOps website at [https://dev.azure.com](https://dev.azure.com), and sign in.

2. On the **Projects** tab, locate the project repo you want to clone, and select the **Repos** icon.

    For example, in the following image, the **Repos** icon for the project **example-repo** is selected.

    ![Example AzDevOps repo project with the 'Repos' icon selected](../assets/images/07-download-files/clone/azdev/az-clone-002.png)

3. Choose the **Clone** icon.

    ![Example AzDevOps repo project with the 'Clone' icon selected](../assets/images/07-download-files/clone/azdev/az-clone-003.png)

4. In the **Clone Repository** pane, set the **IDE** dropdown to **Clone in VS Code**.

    ![The AzDevOps 'Clone Repository' pane, with the 'IDE' dropdown set to 'Clone in VS Code'](../assets/images/07-download-files/clone/azdev/az-clone-004.png)

5. In the **Launch Application** window, set the **Send to** option to **Visual Studio Code**, and then choose **Open link**.

    ![The 'Send to' option set to 'Visual Studio Code' in the 'Launch Application' window](../assets/images/07-download-files/clone/azdev/az-clone-005.png)

6. When the Visual Studio Code editor (VSC) opens, choose **Open** if you're asked to **Allow an Extension to open this URI**.

    ![The 'Send to' option set to 'Visual Studio Code' in the 'Launch Application' window](../assets/images/07-download-files/clone/azdev/az-clone-006.png)

7. In the VSC file explorer, select a location on your computer for storing the cloned repo, and then choose **Select Repository Location**.

    For example, in the following image, the repo will be cloned into the folder **C:\Windows\AzDevOps**.

    ![The 'VSC file explorer' set to clone the example repo into the folder 'C:\Windows\AzDevOp's](../assets/images/07-download-files/clone/azdev/az-clone-007.png)

8. In VSC, wait for the **Cloning git repository** progress indicator to complete (lower right side).

    ![The VSC 'Cloning git repository' progress indicator](../assets/images/07-download-files/clone/azdev/az-clone-008.png)

9. If prompted, sign into AzDevOps/ Visual Studio.

    ![The Visual Studio sign in page](../assets/images/07-download-files/clone/azdev/az-clone-009.png)

10. In VSC, choose **Open** if asked **Would you like to open the cloned repository, or add it...**

    > **Note**: In VSC, you can open a cloned repo from the top menu by using **File** > **Open folder**, and selecting the folder with the cloned repo.
    >

    ![A prompt in VSC to open a cloned repository or add it to the current VSC workspace](../assets/images/07-download-files/clone/azdev/az-clone-010.png)

11. The **branch icon** in the VSC **status bar**, at the bottom of the editor, indicates the name of branch that VSC is currently switched to.

    For example, in the following image, the branch icon in the VSC status bar indicates that VSC is currently switched to the branch named **master**.

    ![Example repo folder open in VSC, and the branch icon in the VSC status bar indicates that VSC is currently switched to the branch named 'master'](../assets/images/07-download-files/clone/azdev/az-clone-011.png)

    > **Note**: To switch VSC to another branch, refer to the guide [Switch branches]({{site.baseurl}}/branches/switch-branch.html).
    >

12. Select the VSC **Explorer icon**, and use the VSC **Explorer** to choose a markdown file to open in the VSC **Editor tab**.

    For example, in the following image, the markdown file **sample-file \.md** is open in the VSC **Editor tab** (right side), and VSC **Explorer** shows that the file is on the filepath **~/example-repo/sample-folder/** (left side).

    ![Example markdown file open in the VSC 'Editor tab', with the filepath in the VSC 'Explorer'](../assets/images/07-download-files/clone/azdev/az-clone-012.png)

You've cloned the project's AzDevOps repo successfully.

{% include appendices.html %}
