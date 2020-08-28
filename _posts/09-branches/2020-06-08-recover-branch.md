---
layout: multi
title: Recover deleted branch
subtitle: GitHub
description: Guide to restoring a deleted branch using GitHub
author: mkavana
date: 01 Jun 2020
post-number: 9.8
category: branches
position-in-category: 8
include-in-pre-reqs: "false"
include-in-quickstart: "false"
video_url: "none"
---

This guide describes how to restore a deleted branch using GitHub.

> **Note**: The following instructions *only* apply to restoring a branch that was merged previously, and then deleted via a Pull Request on GitHub. The process for restoring branches deleted by other means is beyond the scope of this guide.
>
> As an example, this guide uses the WayPoint Ventures' test repository (**Testrepo1**) on GitHub at [https://github.com/WaypointVentures/Testrepo1/](https://github.com/WaypointVentures/Testrepo1/). Modify the following instructions to suit your preferred Git repository (repo).
>

{% include prerequisites.html %}

## Topics in this guide

- [Restore a deleted branch to GitHub](#restore-branch)

{% include video.html %}

## Restore a deleted branch to GitHub {#restore-branch}

Complete the following steps to restore a deleted branch using GitHub.

1. Open a web browser, go to the URL for the project's GitHub repo, and sign in to GitHub.

    For example, go to the WayPoint Ventures' test repository (**Testrepo1**) on GitHub at [https://github.com/WaypointVentures/Testrepo1/](https://github.com/WaypointVentures/Testrepo1/).

2. Select the **Pull requests** tab from the top menu.

    !['Pull requests' tab on GitHub](../assets/images/09-branches/recover/github/recover-002.png)

3. Choose **Closed** from the **Pull request** menu to view a list of all previously closed pull requests.

    !['Closed pull requests' button on gitHub](../assets/images/09-branches/recover/github/recover-003.png)

4. From the list of closed pull requests, select the pull request that contains the deleted branch you want to restore.

    For example, choose **arbitrary edit to README for branch recovery demo** (near the end of the page).

    ![Example closed pull request on GitHub](../assets/images/09-branches/recover/github/recover-004.png)

5. Scroll down through the messages, past the merge point, and select the **Restore branch** button.

    !['Restore branch' button on GitHub](../assets/images/09-branches/recover/github/recover-005.png)

6. Return to the top of the page and select the **Code** tab.

    !['Code' tab button on GitHub](../assets/images/09-branches/recover/github/recover-006.png)

7. Select the **branches dropdown**, and verify that your restored branch is on the list of available branches.

    For example, in the following image, the branch called **DLtest1** is a restored branch.

    !['Branches dropdown' on GitHub](../assets/images/09-branches/recover/github/recover-007.png)

8. Add the restored branch into your local repo with the `git pull` command by following the guide [Update branch (pull)]({{site.baseurl}}/branches/pull-updates.html).

    > **Note**: If you don't have a local repo, create one by cloning the project's GitHub repo using the guide [Download course files (clone repo)]({{site.baseurl}}/download-files/clone-repo.html).
    >

9. After you have pulled the restored branch into your local repo, switch to the restored branch by following the guide [Switch branches]({{site.baseurl}}/branches/switch-branch.html).

You have restored a deleted branch with GitHub successfully.

{% include appendices.html %}

{% include paginator.html %}
