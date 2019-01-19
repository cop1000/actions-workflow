Let's use our first action, [Branch Cleanup](https://github.com/jessfraz/branch-cleanup-action). This action will [delete a branch](https://stackoverflow.com/questions/10765321/should-i-delete-a-branch-after-merging-it) after anyone merges a pull request. The action must be a part of a workflow.

Let's create the workflow. We'll name it, and choose the event that will trigger the workflow. 

Activity: Create the workflow block

1. Click on the **Actions** tab
1. Click **Create a new workflow**
1. Click **Edit** in the New workflow block.
1. Select Run on: **pull_request**
1. Click **Done**.
1. Click **Start commit** on the top right. 
1. Enter a commit message, select Create a new branch, and click **Commit new file**. 
1. On the Open a pull request page, click **Create pull request**. 
1. Title the pull request: **Add branch cleanup workflow**

I'll respond in your new pull request when it is opened. 