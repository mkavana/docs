---
layout: page
title: Fix cloning errors
subtitle: GitHub
description: A guide to fixing common cloning errors
author: mkavana
date: 01 Jun 2020
post-number: 7.4
category: download-files
position-in-category: 4
include-in-pre-reqs: "false"
include-in-quickstart: "false"
video_url: "none"
---

This guide describes how to resolve common errors you might encounter when cloning a fork/ repository (repo) from GitHub.

> **Note**: As an example, this guide uses a fork from the GitHub repo **MicrosoftDocs/learn-pr** from [https://github.com/MicrosoftDocs/learn-pr/](https://github.com/MicrosoftDocs/learn-pr/). Apply this guide to any suitable *private* GitHub repo by adapting the steps accordingly.
>

{% include prerequisites.html %}

## Topics in this guide

- [Repository not found error](#remote-not-found)
- [Enabled or enforced SAML SSO error](#saml-sso-error)
- [Specify Git credentials to use with a clone](#specify-credentials)

{% include video.html %}

## Repository not found error {#remote-not-found}

If you receive the error **Repository not found** while cloning a fork (or any repo), resolve the error by completing the following steps.

The following images are examples of the error **Repository not found** in a Bash Shell (first image), and in Visual Studio Code (second image).

![Example of the error 'Repository not found' in a Bash Shell](../assets/images/07-download-files/clone-error/github/clone-fork-01-01a.png)

.

![Example of the error 'Repository not found' in VSC](../assets/images/07-download-files/clone-error/github/clone-fork-01-01b.png)

1. Ensure you're added as a collaborator to the GitHub fork/ repo you're cloning. If necessary, refer the fork/ repo owner to [Invite collaborator]({{site.baseurl}}/add-content/invite.html).

    > **Note** You might have more than one email address associated with your GitHub user account(s). For example, one for Waypoint and one for your **v-**. If you *do* have more than one, *ensure the fork/ repo owner sends their invitation to the correct GitHub username*. For example, to contribute to Microsoft Docs, have the invitation sent to your GitHub username that's linked to your **v-**.
    >

2. Confirm you've accepted the fork/ repo owner's invitation to collaborate.

3. Clone the repo again by referring to the guides [Download course files (clone repo)]({{site.baseurl}}/download-files/clone-repo.html) and [Fork a repository]({{site.baseurl}}/download-files/fork-repo.html).

## Enabled or enforced SAML SSO error {#saml-sso-error}

If you receive the error **Enabled or enforced SAML SSO** while cloning a fork (or any repo), resolve the error by completing the following steps.

> **Note**: Ensure you're added as a collaborator to the GitHub fork/ repo you're cloning. If necessary, refer the fork/ repo owner to [Invite collaborator]({{site.baseurl}}/add-content/invite.html).
>

The following image is an example of the error **Enabled or enforced SAML SSO** in a Bash Shell.

![Example of the error 'Enabled or enforced SAML SSO' in a Bash Shell](../assets/images/07-download-files/clone-error/github/clone-fork-02-00.png)

1. Open a web browser, go to [GitHub.com](https://github.com), and sign in.

2. Go to the error message in your Shell or Visual Studio Code, copy the URL from the SAML SSO error, and then paste the URL into a web browser.

    For example, in the following image, the URL to copy is:

    `https://github.com/microsoftopensource/sso?authorization_request=XXXX0X0XXXXX0X0X0XXXXXXX ...`

    ![Example URL to copy from a SAML SSO error in a Bash shell](../assets/images/07-download-files/clone-error/github/clone-fork-02-02.png)

3. In your browser, if prompted, confirm that you want to add your GitHub username and email address to the Microsoft Docs organization on GitHub.

4. After you follow the URL link, and join the Microsoft Docs GitHub organization, clone the GitHub fork/ repo again by referring to the guides [Download course files (clone repo)]({{site.baseurl}}/download-files/clone-repo.html) and [Fork a repository]({{site.baseurl}}/download-files/fork-repo.html).

> **Note**: A fork of a Microsoft Docs GitHub repo usually inherits any membership rules from the fork's "parent". For example, the GitHub repo **MicrosoftDocs/learn-pr** requires contributors to be members of the Microsoft Docs organization on GitHub. Forks created from *MicrosoftDocs/learn-pr* will inherit this requirement. If you clone a fork of *MicrosoftDocs/learn-pr*, to modify files in your fork, your GitHub user account *must* be a member of the Microsoft Docs GitHub organization.
>
> If visiting the URL you pasted does not resolve the SAML SSO errors, refer to [Specify Git credentials to use with a clone](#specify-credentials).
>

# Specify Git credentials to use with a clone {#specify-credentials}

If you're a confirmed collaborator to the GitHub fork/ repo you're cloning, and a member of any required organizations like the Microsoft Docs GitHub organization, but you still receive cloning errors, your (default) Global Git credentials might not have permission to clone the fork/ repo.

Complete the following steps to override your default Git credentials by specifying the particular Git credentials to use with the fork/ repo you're cloning.

1. Open a web browser, go to [GitHub.com](https://github.com), and sign in.

2. On GitHub, go to the URL for the fork/ repo you're cloning at:

    `https://github.com/ fork or repo owner's GitHub username/ fork or repo name/`.

3. Select **Code**, and copy the URL link to your clipboard.

    ![Code button in an example GitHub repo](../assets/images/07-download-files/clone-error/github/clone-fork-03-03a.png)

    ![Sample URL used for cloning, in an example GitHub repo](../assets/images/07-download-files/clone-error/github/clone-fork-03-03b.png)

4. On your computer, open a Shell, like **Command prompt** (cmd), **PowerShell**, **Bash**, or **VSC Terminal**. Then, enter the following commands into the Shell. Use **ENTER** *after* each command.

5. Change directory (`cd`) into where you want to clone the fork/ repo onto your computer.

    ```bash
    cd path/to/folder/to-clone-into
    ```

    ![Bash shell running the 'cd' command](../assets/images/07-download-files/clone-error/github/clone-fork-03-05.png)

    For example, in the previous image, the Bash Shell is changing directory into the folder **c:\myGitFolder**.

6. Create (initialize) a new empty Git repository inside the current folder on your computer (i.e. initialize a new local repo).

    ```bash
    git init .
    ```

    ![Bash shell running the Git 'init' command](../assets/images/07-download-files/clone-error/github/clone-fork-03-06.png)

    For example, in the previous image, a new empty Git repository is created in the folder **c:\myGitFolder**.

7. Set your username (an alias) for Git to use with the new Git repo you created.

    ```bash
    git config user.name "Your Name Here"
    ```

    ![Bash shell running the Git 'set username' command](../assets/images/07-download-files/clone-error/github/clone-fork-03-07.png)

    For example, in the previous image, the alias **Your Name Here** is used with the new Git repo created previously.

8. Set the email address for Git to use with the repo you created.

    > **Note**: Replace **your@email.com** with your email address *that the fork/ repo owner used to invite you as a collaborator on GitHub*.
    >

    ```bash
    git config user.email your@email.com
    ```

    ![Bash shell running the Git 'set user email address' command](../assets/images/07-download-files/clone-error/github/clone-fork-03-08.png)

    For example, in the previous image, the email address **user.email your@email.com** is used with Git repo created previously.

9. Add the GitHub fork/ repo you're cloning as a remote for the repo you created. Paste the URL link you copied to your clipboard in **Step 3**.

    ```bash
    git remote add origin https://github.com/ fork or repo owners GitHub username/ fork or repo name.git
    ```

    ![Bash shell running the Git 'add remote' command](../assets/images/07-download-files/clone-error/github/clone-fork-03-09.png)

    For example, in the previous image, the GitHub fork `https://github.com/mkavana/learn-pr.git` is added as a remote to the repo created previously.

10. Download (pull) the contents of the (remote) GitHub fork/ repo into the repo you created.

    ```bash
    git pull origin master
    ```

    ![Bash shell running the Git 'pull remote' command](../assets/images/07-download-files/clone-error/github/clone-fork-03-10a.png)

    For example, in the previous image, the contents the GitHub fork `https://github.com/mkavana/learn-pr.git` are pulled into the local repo.

    In the following image, the content pulled from the GitHub fork are now accessible from **Windows Explorer** in a local repo on the filepath **C:\myGitFolder\learn-pr**.

    ![Contents of an example Git repo in Windows Explorer](../assets/images/07-download-files/clone-error/github/clone-fork-03-10b.png)

> **Note**: If your receive further SAML SSO errors, refer to [Enabled or enforced SAML SSO error](#saml-sso-error).
>

{% include appendices.html %}

{% include paginator.html %}
