---
layout: page
title: Install Pull Requests extension
subtitle: GitHub repositories only
description: Guide to downloading and installing the GitHub Pull Requests and Issues extension for Visual Studio Code.
author: mkavana
date: 01 Jun 2020
post-number: 3.4
category: install
position-in-category: 4
include-in-pre-reqs: "true"
include-in-quickstart: "true"
video_url: "none"
---

This guide describes how to download and install the **GitHub Pull Requests and Issues** extension for Visual Studio Code (VSC). The extension connects VSC to GitHub for managing changes made to the course files from within VSC.

> **Note**: Only complete this guide if the course you are working on uses a GitHub repository. The extension described in this guide is *not required* for courses that use an Azure DevOps repository. If you are unsure, check with your project manager.
>
> More information about the extension is available from the Visual Studio Marketplace webpage [GitHub Pull Requests and Issues](https://marketplace.visualstudio.com/items?itemName=GitHub.vscode-pull-request-github).

{% include prerequisites.html %}

## Topics in this guide

- [Topic 1: Download and install the GitHub Pull Requests and Issues extension](#topic1)

{% include video.html %}

## Topic 1: Download and install the GitHub Pull Requests and Issues extension {#topic1}

Complete the following steps to download and install the GitHub Pull Requests and Issues extension for VSC.

1. Launch VSC.

2. Choose the **Extensions** icon from the left sidebar menu.

    ![Extensions icon from the VSC left sidebar menu](../assets/images/03-install/pr-ext/pr-ext-002.png)

3. Type **Github pull requests and Issues** into the extensions search text entry field.

    ![VSC extensions search text entry field](../assets/images/03-install/pr-ext/pr-ext-003.png)

4. The **Github pull requests and Issues** extension should appear near the top of the list of search results.

    Verify that the publisher name is **GitHub**, and select the green **install** button inside the **Github pull requests and Issues** extension information panel (lower right side).

    ![Install button inside the Github pull requests and Issues extension information panel in VSC](../assets/images/03-install/pr-ext/pr-ext-004.png)

5. When prompted to sign in to GitHub, choose the **Sign in** button from the dialog box (lower right side).

    ![Sign in to GitHub dialog box from the Github pull requests and issues vsc extension installer](../assets/images/03-install/pr-ext/pr-ext-005.png)

6. Select **Allow** from the new window that appears.

    Note the **Signing into...** message in the VSC status bar (bottom of the VSC editor window).

    ![Prompt to confirm allowing vsc to sign into GitHub](../assets/images/03-install/pr-ext/pr-ext-006.png)

7. Your web browser should open the GitHub sign in webpage automatically.

    > **Note**: If prompted, choose your preferred web browser from the list, for example **Microsoft Edge**, then select **OK**.
    >
    > ![Prompt to choose a web browser during the installation of the Github pull requests and issues vsc extension](../assets/images/03-install/pr-ext/pr-ext-007.png)

8. In your web browser, choose **Continue** from the webpage **Authorize Visual Studio Code to access GitHub** to allow VSC to connect to your GitHub user account.

    ![Webpage to confirm that vsc is authorized to access GitHub ](../assets/images/03-install/pr-ext/pr-ext-008.png)

9. In your web browser, when prompted, enter your GitHub username and password, then choose **Sign in**.

    ![GitHub user sign in prompt](../assets/images/03-install/pr-ext/pr-ext-009.png)

10. In your web browser, when prompted, verify that your GitHub user account is listed on the **Authorize GitHub for VSCode** webpage. Then, choose **Authorize github**.

    ![The Authorize GitHub for VSCwebpage with an example GitHub user account](../assets/images/03-install/pr-ext/pr-ext-010.png)

11. Your web browser should open the **Success!** webpage, with a message indicating that **Authorization was successful**.

    ![Webpage confirming that VSC was authorized to connect to GitHub successfully](../assets/images/03-install/pr-ext/pr-ext-011.png)

12. Return to VSC and, if prompted, choose **Visual Studio Code** from the **Launch Application** dialog box. Then, select **Open link**.

    ![Launch Application dialog box with VSC selected](../assets/images/03-install/pr-ext/pr-ext-012.png)

13. When prompted to **Allow an extension to open this URI?**, choose **Open** from the **Visual Studio Code** dialog box.

    ![Prompt requesting that a VSC extension be allowed to open a URI](../assets/images/03-install/pr-ext/pr-ext-013.png)

14. When the GitHub Pull Requests and Issues extension has installed successfully the installation status icon text, inside the extension details pane, will change from **Install** (with a green coloured icon) to **Uninstall** (a blue coloured icon).

    ![Extension installation status icon inside the VSC extension details pane](../assets/images/03-install/pr-ext/pr-ext-014a.png)

    The **Signing into...** message will disappear from the VSC status bar (at the bottom of the VSC editor window).

    ![VSC status bar without the 'Signing into...' message](../assets/images/03-install/pr-ext/pr-ext-014b.png)

    > **Note**: If the installation fails, return to your web browser and follow the steps described in the **Didn't work?** section of the **Success!** webpage (to add an authorization token to VSC manually).
    >
    > ![Webpage with instructions for adding an authorization token to VSC manually](../assets/images/03-install/pr-ext/pr-ext-015.png)

You have downloaded and installed the GitHub Pull Requests and Issues extension successfully.

{% include appendices.html %}

{% include paginator.html %}
