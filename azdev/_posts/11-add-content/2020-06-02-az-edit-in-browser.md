---
layout: multi
title: Add/ edit content in web browser
subtitle: AzDevOps
description: A guide to using a web browser to edit, or add content into, a markdown file on AzDevOps
author: mkavana
date: 01 Jun 2020
post-number: 11.2
#category: add-content
#position-in-category: 2
include-in-pre-reqs: "false"
include-in-quickstart: "false"
include-in-azdevops-quickstart: "false"
video_url: "none"
---

This guide describes using a web browser to edit, or add content into, a markdown file on AzDevOps.

> **Note**: This guide assumes that the markdown file you're modifying exists on AzDevOps already. As an example, this guide uses a markdown file from an example repository (**example-repo**) on AzDevOps. Modify the following instructions to suit your preferred markdown file and AzDevOps repository (repo) accordingly.
>

{% include prerequisites.html %}

## Topics in this guide

- [Edit a markdown file on AzDevOps in a web browser](#az-edit-browser)

{% include video.html %}

## Edit a markdown file on AzDevOps in a web browser {#az-edit-browser}

Complete the following steps to use a web browser to modify a markdown file on AzDevOps.

1. Open a web browser, go to the AzDevOps website at [https://dev.azure.com](https://dev.azure.com), and sign in.

    ![alt text](../assets/images/11-add-content/edit-browser/azdev/az-edit-browser-001.png)

2. On the projects tab, locate the project you require, and select the **Repos** icon.

    For example, in the following image, the **Repos** icon for the project **example-repo** is selected.

    ![Example AzDevOps repo project with the 'Repos' icon selected](../assets/images/11-add-content/edit-browser/azdev/az-edit-browser-002.png)

3. The **branch dropdown** indicates which branch AzDevOps is currently set to.

    For example, in the following image, the branch dropdown indicates that AzDevOps is set to the branch named **master**.

    ![Example AzDevOps repo with the 'branch dropdown' set to the 'master' branch](../assets/images/11-add-content/edit-browser/azdev/az-edit-browser-003a.png)

    Use the **branch dropdown** to view a list of available branches, and then choose the branch with the file you want to modify.

    For example, in the following image, the branch **mod01-ce-mkavana** is selected from the **branch dropdown**.

    ![Example AzDevOps repo with the 'branch dropdown' set to the branch 'mod01-ce-mkavana'](../assets/images/11-add-content/edit-browser/azdev/az-edit-browser-003b.png)

4. Select **Files** from the left sidebar to access the repo's contents.

    ![Example AzDevOps repo 'Files' selected from the left sidebar menu](../assets/images/11-add-content/edit-browser/azdev/az-edit-browser-004.png)

5. The AzDevOps repo uses a standard file and folder structure. Browse the repo's contents, and go to the folder and file you require.

    For example, in the following image, the file **sample-file \.md** is selected in the folder **mod01-folder**.

    ![Example AzDevOps repo with branch name and filepath](../assets/images/11-add-content/edit-browser/azdev/az-edit-browser-005a.png)

    > **Note**: Use your web browser's address bar to get the URL for a file on AzDevOps. The URL contains the path to the file and the branch name. You can share the URL with other contributors if you need to.
    >
    > For example, in the following image, the URL in the address bar is selected for copying the filepath **mod01-folder\sample-file \.md** on the branch named **mod01-ce-mkavana**.
    >
    > ![Example AzDevOps repo with a sample URL in the address bar for a sample branch name and filepath](../assets/images/11-add-content/edit-browser/azdev/az-edit-browser-005b.png)
    >

6. Select **Edit** (the **pencil icon**) to open the file in the **Editor** pane.

    For example, in the following image, the **Edit** icon opens the markdown file **sample-file \.md** in the **Editor** pane.

    !['Edit' icon on AzDevOps to select an example markdown file for editing](../assets/images/11-add-content/edit-browser/azdev/az-edit-browser-006.png)

7. In the **Contents** tab, locate the part of the markdown file you want to modify.

    For example, in the following image, part of the file below the heading **`## 02. Example topic`** is selected.

    !['Contents' tab on AzDevOps with part of an example markdown file selected for editing](../assets/images/11-add-content/edit-browser/azdev/az-edit-browser-007.png)

8. Apply the required edits or add your content to the markdown file.

    For example, the following text is added into the last line of the markdown file **sample-file \.md**.

    ```markdown
    This is sample text.
    ```

    ![Sample text added into the example markdown on AzDevOps](../assets/images/11-add-content/edit-browser/azdev/az-edit-browser-008.png)

    > **Note**: Ensure that your file modifications conform to the markdown syntax described in the guide [Markdown syntax guide]({{site.baseurl}}/add-content/syntax.html).
    >

9. To preview how your file modifications are rendered, choose the **Preview** tab. To return to editing the file, select the **Contents** tab.

    > **Note**: Previewing your file changes is optional, but considered good practice as it helps you to ensure that your file changes render as intended.
    >

    For example, in the following image, the **Preview** tab in the AzDevOps editor contains the text added into markdown file **sample-file \.md**.

    !['Preview' tab in the AzDevOps editor with text added into the example markdown file](../assets/images/11-add-content/edit-browser/azdev/az-edit-browser-009.png)

10. After you've made the necessary file edits/ additions, select **Commit**.

    !['Commit' button in the AzDevOps editor](../assets/images/11-add-content/edit-browser/azdev/az-edit-browser-010.png)

11. In the **Commit** pane, complete the following:

    |Item|Description|
    |---|---|
    |**Comment**|Add a message to provide other contributors with a summary description of the changes you applied to the file. For example, *add new sample text to the file 'mod01-folder/sample-file.md'*|
    |**Branch name**|To save (commit) your file changes to a new branch, enter a name for your new branch. For example, **mod01-text-update-mk**. In the next steps, you'll ask the owner of the originating branch to approve and accept your file changes by using pull request (preferred approach).|

    For example, in the following image, the message in the **Commit** pane describes the text added to the example markdown file (in the previous **Step 8**). The file change will be committed to a *new* branch named **mod01-text-update-mk**.

    !['Commit' pane in the AzDevOps editor with a description changes applied to the example markdown file on a new branch](../assets/images/11-add-content/edit-browser/azdev/az-edit-browser-011a.png)

    > **Note**: Using a pull request (PR) to ask the owner of the originating branch to approve your file changes is the preferred approach. Alternatively, you can commit your file changes directly to the current branch without opening a new pull request. Committing file changes directly to an existing branch is *not recommended* as it makes tracking changes and fixing problems more difficult. Always create a new branch and open a pull request, unless you *must* commit to the current branch directly (for example, during a Technical Review).
    >
    > To commit to the current branch, after you add your commit message, leave the branch name set to the current branch, choose **Commit**, and then skip ahead to Step **19**.
    >
    > For example, in the following image, the message in the **Commit** pane describes the text added to the example markdown file (in the previous **Step 8**). The file change will be committed to the *current* branch **mod01-ce-mkavana**.
    >
    > !['Commit' pane in the AzDevOps editor with a description changes applied to the example markdown file on the current branch](../assets/images/11-add-content/edit-browser/azdev/az-edit-browser-011b.png)
    >

12. Use the checkbox to select the option to **Create a pull request**. Then, choose **Commit**.

    !['Create a pull request' checkbox option selected in the AzDevOps editor](../assets/images/11-add-content/edit-browser/azdev/az-edit-browser-012.png)

13. In the **New pull request** form, use the dropdowns to set the branch to merge *from* and the branch to merge *into*.

    For example, in the following image, the dropdowns are set to merge *from* the branch **mod01-text-update-mk** *into* the branch **mod01-ce-mkavana**.

    ![Example PR on the AzDevOps with the merge to and from branches set using dropdown options](../assets/images/11-add-content/edit-browser/azdev/az-edit-browser-013.png)

14. In the **New pull request** form, add the following into the PR **Title** text field:

    - number of the module that the file you're merging belongs to
    - type of action you performed on the file you're merging (for example, copy edit review, image updates)
    - name of the branch you're merging *into* (for example, master)

    For example, in the following image, a suitable PR title is **Mod01 text updates merge from branch 'mod01-ce-mkavana' into branch 'mod01-ce-mkavana'**.

    ![Example PR title on the AzDevOps 'New pull request' page](../assets/images/11-add-content/edit-browser/azdev/az-edit-browser-014.png)

15. **Optional**: In the **Description** text field, describe the file additions/ changes you're merging.

    For example, in the following image, a suitable description is **Add new sample text into the Mod01 file 'mod01-folder/sample-file.md'**.

    ![Example description on the AzDevOps 'New pull request' page](../assets/images/11-add-content/edit-browser/azdev/az-edit-browser-015.png)

    > **Note**: Descriptions provide a way for contributors to explain the changes they apply to files. Descriptions are *optional*, but recommended.
    >
    > The reviewer's guides in the **Workflow and processes** section of this website suggest adding a checklist of items the for review into the **Description** field. A checklist provides a convenient way for reviewers, content authors, and other contributors to track the progress of a review. To add a review checklist to your PR, choose a guide that corresponds to your role from the **navigation menu** on the left of this website.
    >

16. For **Reviewers**, add a reviewer to your PR by entering the reviewer's AzDevOps username, and then select the reviewer's username from the list.

    It's good practice to add the owner of the branch you're merging into as a reviewer, like the originating author for example. If you modify files in the PR, AzDevOps will send notifications to all the users you add as reviewers.

    ![The 'Reviewers' pane in an example pull request tab on AzDevOps](../assets/images/11-add-content/edit-browser/azdev/az-edit-browser-016.png)

17. Select **Create**.

    ![The 'Create' button in the new pull request pane on AzDevOps](../assets/images/11-add-content/edit-browser/azdev/az-edit-browser-017.png)

18. The **Overview** pane contains details of your pull request, and confirms you've created a new pull request successfully.
  
    ![The 'Overview' pane with details of an example pull request pane on AzDevOps](../assets/images/11-add-content/edit-browser/azdev/az-edit-browser-018.png)

    > **Note**: For more information about pull requests, refer to [Pull requests overview]({{site.baseurl}}/pull-requests/pr-overview.html).
    >

19. Send an email to the person you're handing your files off to (as a notification that your PR is ready). Your email should include the following:

    - Details about the PR (like the names of the branches the PR involves, PR title, number, and purpose). For example, **Mod01 text updates merge from branch 'mod01-ce-mkavana' into branch 'mod01-ce-mkavana'**
    - URL/ link to the PR on AzDevOps (refer to the previous Step **5**)
    - **Optional**: Screen capture/ grab of the PR

You've used a web browser to modify a markdown file on AzDevOps successfully.

{% include appendices.html %}
