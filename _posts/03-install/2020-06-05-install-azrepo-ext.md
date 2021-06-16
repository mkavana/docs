---
layout: page
title: Install Azure Repos extension
subtitle: Azure DevOps repositories only
description: Guide to downloading and installing Microsoft's Azure Repos extension
author: mkavana
date: 01 Jun 2020
post-number: 3.5
category: install
position-in-category: 5
include-in-pre-reqs: "true"
include-in-quickstart: "false"
include-in-azdevops-quickstart: "true"
video_url: "none"
---

This guide describes how to download and install Microsoft's **Azure Repos** extension for Visual Studio Code (VSC). The extension connects VSC to Azure DevOps for managing changes made to the course files from within VSC.

> **Note**: Only complete this guide if the course you are working on uses an Azure DevOps repository. The extension described in this guide is *not required* for courses that use a GitHub repository. If you are unsure, check with your project manager.
>
> More information about the extension is available from the Visual Studio Marketplace webpage [Azure Repos](https://marketplace.visualstudio.com/items?itemName=ms-vsts.team).

## Important update

Microsoft removed the Azure Repos VSC extension from Visual Studio Marketplace on Nov 6 2020, refer to [https://github.com/microsoft/azure-repos-vscode/blob/master/DEPRECATED.md](https://github.com/microsoft/azure-repos-vscode/blob/master/DEPRECATED.md).

Despite this, some Microsoft projects use Team Foundation with Azure DevOps for version control, instead of Git and GitHub. If you work with these projects, you might need to install the Azure Repos VSC extension. Ask your project manager if the project you're working on requires the Azure Repos extension.

You can no longer install the extension from Visual Studio Marketplace (as described in this guide). Instead, complete the following steps to obtain and install the extension.

1. In a web browser, go to [https://marketplace.visualstudio.com/items?itemName=ms-vsts.team](https://marketplace.visualstudio.com/items?itemName=ms-vsts.team).

2. Choose the **Version History** tab.

3. Select **Download**, beside version **1.161.1**, and save the file `ms-vsts.team-1.161.1.vsix` to your computer.

4. Open VSC, and then select **Terminal** > **New Terminal** or use **CRTL** + **SHIFT** + **'**.

5. In the terminal, navigate to where you saved `ms-vsts.team-1.161.1.vsix`.

6. Enter the following command to install the extension:

    ``````bash
    code --install-extension ms-vsts.team-1.161.1.vsix
    ``````

> **Note**: You can ignore warnings in VSC about using a depreciated ("sunsetted") extension.
>
> For help, refer to the Visual Studio Code documentation article [Install from a VSIX](https://code.visualstudio.com/docs/editor/extension-marketplace#_install-from-a-vsix).
>

{% include prerequisites.html %}

## Topics in this guide

- [Download and install Microsoft's Azure Repos extension](#install-az-repos)

{% include video.html %}

## Download and install Microsoft's Azure Repos extension {#install-az-repos}

Complete the following steps to download and install Microsoft's Azure Repos extension for VSC.

1. Launch VSC.

2. Choose the **Extensions** icon from the left sidebar menu.

    ![Extensions icon from the VSC left sidebar menu](../assets/images/03-install/azrepo-ext/azrepo-002.png)

3. Type **azure repos** into the extensions search text entry field.

    ![VSC extensions search text entry field](../assets/images/03-install/azrepo-ext/azrepo-003.png)

4. The **Azure Repos** extension should appear near the top of the list of search results.

    Verify that the publisher name is **Microsoft**, and select the green **install** button inside the Microsoft **Azure Repos** extension information panel (lower right side).

    ![Install button inside the Microsoft Azure Repos extension information panel in VSC](../assets/images/03-install/azrepo-ext/azrepo-004.png)

5. When the Microsoft **Azure Repos** extension has installed successfully the installation status icon text, inside the extension details pane, will change from **Install** (with a green coloured icon) to **Uninstall** (a blue coloured icon).

    ![Uninstall icon, inside the extension details pane in VSC](../assets/images/03-install/azrepo-ext/azrepo-005.png)

6. To complete the installation, restart VSC by choosing **File** > **Exit** (from the top VSC menu), then re-opening VSC.

    ![File menu in VSC](../assets/images/03-install/azrepo-ext/azrepo-006.png)

You have downloaded and installed the Microsoft Azure Repos extension for VSC successfully.

{% include appendices.html %}

{% include paginator.html %}
