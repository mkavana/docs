---
layout: multi
title: Resolve merge conflicts
subtitle: GitHub
description: A guide to resolving merge conflicts
author: mkavana
date: 01 Jun 2020
post-number: 13.5
category: pull-requests
position-in-category: 5
include-in-pre-reqs: "false"
include-in-quickstart: "false"
video_url: "none"
---

This guide describes merge conflicts, and how to resolve a simple merge conflict on GitHub.

{% include prerequisites.html %}

## Topics in this guide

- [An overview of merge conflicts](#merge-conflicts-overview)
- [Resolve a simple merge conflict on GitHub](#merge-conflicts-steps)

{% include video.html %}

## An overview of merge conflicts {#merge-conflicts-overview}

Git users can work in the same file on different branches concurrently. For example, two Git users working on different branches can edit **line number 100** in the file **example \.md**, at the same time, and then push their edited files "up" to GitHub.

Merge conflicts arise from attempts to merge branches that contain incompatible versions of the same file. Staying with the previous example, there is different content on **line number 100** in the file **example \.md** on each of the two users' branches. Pushing the files to GitHub creates two competing versions of the file  **example \.md**. When you try to merge the branches, Git doesn't know which version of the file to merge. The result is an error called a "merge conflict".

### About complex and simple merge conflicts

Resolving a merge conflict requires "human intervention" to tell Git which version of the file to merge. All merge conflicts *must* be resolved before GitHub will allow you to merge a pull request (PR). On the GitHub **Pull requests** tab, if you attempt to merge a PR with conflicting files, GitHub displays a warning message, lists the conflicting files, and deactivates the **Merge pull request** button. The **Merge pull request** button remains deactivated until you've resolved the merge conflicts.

![Merge conflict warning on GitHub](../assets/images/13-pull-requests/conflicts/github/pr-conflict-001.png)

> **Note**: For more information about merge conflicts, refer to the GitHub documentation page [About merge conflicts](https://docs.github.com/github/collaborating-with-issues-and-pull-requests/about-merge-conflicts).
>

There are many causes of merge conflicts. For complex merge conflicts, you must identify the cause of the conflict and implement an appropriate solution. Resolving complex merge conflicts is beyond the scope of this guide. To resolve a complex merge conflict, refer to the GitHub documentation page [Resolving a merge conflict using the command line](https://docs.github.com/github/collaborating-with-issues-and-pull-requests/resolving-a-merge-conflict-using-the-command-line).

Competing line changes, like in the previous example, are a common cause of simple merge conflicts. To resolve a simple merge conflict, caused by competing line changes, follow the steps in [Resolve a simple merge conflict on GitHub](#merge-conflicts-steps).

## Resolve a simple merge conflict on GitHub {#merge-conflicts-steps}

1. In a web browser, sign into GitHub, and go to the project's GitHub repository (remote repo).

    For example, in the following image, the repo (**test-repo**) is open on GitHub.

    ![Example GitHub repo in a web browser](../assets/images/13-pull-requests/conflicts/github/conflict-github-001.png)

2. Select the **Pull requests** tab.

    ![GitHub 'Pull requests' tab](../assets/images/13-pull-requests/conflicts/github/conflict-github-002.png)

3. From the list of **open** PRs, choose the PR with the merge conflict to be resolved.

    ![Example PR selected in the GitHub 'Pull requests' tab](../assets/images/13-pull-requests/conflicts/github/conflict-github-003.png)

4. In the PR **Conversation** tab, scroll down, and then select the button **Resolve conflicts**.

    ![GitHub conversation tab with 'Merge pull request' button](../assets/images/13-pull-requests/conflicts/github/conflict-github-004.png)

    > **Note**: If the button **Resolve conflicts** is deactivated, the merge conflict cannot be resolved on GitHub. To resolve the conflict, refer to the GitHub documentation page [Resolving a merge conflict using the command line](https://docs.github.com/github/collaborating-with-issues-and-pull-requests/resolving-a-merge-conflict-using-the-command-line).
    >

5. The **GitHub editor** opens the conflicting file on the line that contains the first conflict (a "line conflict").

    In the following markdown syntax example, like in the **GitHub editor** panel, the conflicting branches are named, and the conflicting line content is enclosed by the **conflict markers** ``<<<<<<< ======= >>>>>>>``.

    ```markdown
    <<<<<<< conflicting branch name 1

    conflicting line on branch 1
    =======
    conflicting line on branch 2

    >>>>>>> conflicting branch name 2
    ```

    For example, in the following image, the **conflict markers** indicate where the line conflict occurs between the branch **edit-m02-l02** and the branch **master**, in the file **A0001-Mod02-L01-T01_example \.md**.

    ![Example line conflict in a markdown file enclosed by conflict markers on GitHub](../assets/images/13-pull-requests/conflicts/github/conflict-github-005.png)

    Determine which of the conflicting branches has the line content you want to keep. Alternatively, make a new change that incorporates the line content of both conflicting branches by typing into the **GitHub editor** directly.

6. Apply your changes in the **GitHub editor**.

    ![Example changes applied to a markdown file in the GitHub editor, to resolve a line conflict, enclosed by conflict markers](../assets/images/13-pull-requests/conflicts/github/conflict-github-006.png)

7. Delete the conflict markers from around the changes you applied.

    ![Example changes applied to a markdown file in the GitHub editor, to resolve a line conflict, without conflict markers](../assets/images/13-pull-requests/conflicts/github/conflict-github-007.png)

    > **Note**: Repeat steps **4** to **7** to resolve each line conflict in the file. Navigate between conflicting lines within a file by selecting **Prev** and **Next**.
    >

8. When you've resolved all of the line conflicts in the file, choose **Mark as resolved**.

    ![The 'mark as resolved' button on GitHub, with a list of conflicted files beside the 'GitHub editor' panel](../assets/images/13-pull-requests/conflicts/github/conflict-github-008.png)

    > **Note**: Repeat steps **4** to **8** to resolve all conflicts in every conflicted file in the PR. The conflicted files are listed to the left of the **GitHub editor** panel.
    >

9. When you've resolved all conflicts, select **Commit merge** to merge the updated branch.

    ![The 'Commit merge' button on GitHub](../assets/images/13-pull-requests/conflicts/github/conflict-github-009a.png)

    > **Note**: Your changes will be committed to the repo's **head** branch (usually the **master** branch).
    >
    > Depending on your branch policy, and the original PR configuration, you might be prompted to choose a branch to commit your changes to. If you can't or don't want to commit your changes to the head branch directly, select the option to **Create a new branch for this commit...**, then enter a branch name, and choose **Create branch and update my pull request**. GitHub will update the base branch for the PR you're merging accordingly.
    >
    > ![Option to 'Create a new branch...' on GitHub](../assets/images/13-pull-requests/conflicts/github/conflict-github-009b.png)
    >

10. In the **Conversation** tab for the PR, scroll down to the message **This branch has no conflicts with the base branch**, and verify that the option is enabled to **Merge pull request**.

    ![The message 'This branch has no conflicts...' with the option enabled to 'Merge pull request' on GitHub](../assets/images/13-pull-requests/conflicts/github/conflict-github-010.png)

    > **Note**: If GitHub indicates that there are merge conflicts, repeat steps **2** to **9** in this guide until all conflicts are resolved, and then try merging the PR again.
    >

11. With the **Merge pull request** option enabled, merge the PR as normal by following the guide [Merge a pull request]({{site.baseurl}}/pull-requests/merge-pr.html).

You have resolved a simple merge conflict on GitHub successfully.

{% include appendices.html %}

{% include paginator.html %}
