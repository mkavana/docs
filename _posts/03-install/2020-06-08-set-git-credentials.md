---
layout: page
title: Set Git credentials
subtitle:
description: Guide to configuring global user credentials for Git
author: mkavana
date: 01 Jun 2020
post-number: 3.8
category: install
position-in-category: 8
include-in-pre-reqs: "true"
include-in-quickstart: "true"
include-in-azdevops-quickstart: "true"
video_url: "none"
---

This guide describes how to set your global Git user credentials using the Visual Studio Code (VSC) editor.

These steps are *required* to enable persistent interactions between Git, GitHub, Azure DevOps and VSC. Setting your global Git user credentials will distinguish your contributions to the course content from the contributions of others.

{% include prerequisites.html %}

## Topics in this guide

- [Set your Git global credentials](#set-credentials)

{% include video.html %}

## Set your Git global credentials {#set-credentials}

Complete the following steps to set your global Git user credentials using VSC.

1. Open VSC, and go to **View** > **Terminal** (from the top menu). In the VSC **TERMINAL** pane, select **1:powershell** from the dropdown menu.

    > **Note**: You may need to press **Enter** to display the contents of the VSC Terminal window. Your Git username will be shown in the VSC Terminal instead of the username shown in following images.

    ![VSC terminal window opened using the top menu in VSC](../assets/images/03-install/git-credentials/credentials-001.png)

2. Type the following command into the **VSC Terminal**, then press **Enter**.

    ```bash
    git config --list
    ```

    ![VSC terminal running the command 'git config --list' with the Git email and username values missing](../assets/images/03-install/git-credentials/credentials-002.png)

    Note how there are no references to `user.name` or `email.address` present in the **VSC Terminal**. This will change when you add your Git user credentials using the following steps.

3. To configure your global Git user email address, type the following command into the **VSC Terminal** then press **Enter**. Replace the text "**you @example.com**" with the email address you use with your GitHub user account.

    ```bash
    git config --global user.email "you@example.com"
    ```

    ![VSC terminal running the command 'git config --global user.email'](../assets/images/03-install/git-credentials/credentials-003.png)

4. To configure your global Git username, type the following command into the **VSC Terminal** then press **Enter**. Replace the text "**Your Github account user name**" with the Git username you want to be identified by.

    ```bash
    git config --global user.name "Your GitHub account user name"
    ```

    ![VSC terminal running the command 'git config --global user.name'](../assets/images/03-install/git-credentials/credentials-004.png)

5. Type the following command into the **VSC Terminal**, and press **Enter**.

    ```bash
    git config --list
    ```

    ![VSC terminal running the command 'git config --list' with the Git email and username values now present](../assets/images/03-install/git-credentials/credentials-005.png)

    Note how the values for `user.name` and `email.address` are now present in the **VSC Terminal**.

You have set your global Git user credentials successfully. Close the **VSC Terminal** pane and the VSC editor.

> **Note**: VSC does not verify the global Git user credentials you provide. Errors that mention permissions when you use Git may be caused by incorrect or misconfigured Git user credentials. Ensure you have the correct global Git user credentials and GitHub user account details in your Git configuration file (*Git config*). In Windows, the **Git config** file is stored at `C:\Program Files\Git\etc\gitconfig`.
>
> More information about configuring Git is available from the SCM webpage [8.1 Customizing Git - Git Configuration](https://www.git-scm.com/book/en/v2/Customizing-Git-Git-Configuration).

{% include appendices.html %}

{% include paginator.html %}
