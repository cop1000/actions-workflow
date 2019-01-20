Let's create a deployment workflow. We want to deploy anytime we push, so let's ensure we select the `push` event to trigger the workflow.

1. Click on the **Actions** tab
1. Click **Create a new workflow**
1. Click **Edit** in the New workflow block.
1. Select Run on: **push**
1. Click **Done**. 
1. Drag the connector from the workflow block to the outlined action block for the action.
1. In the Choose action field, type `actions/zeit-now@master`.
1. Click **Use**.
1. In the label field, type `deploy`
1. Click **Done**.
1. Click **Start commit** on the top right. 
1. Enter a commit message, select Create a new branch, and click **Commit new file**. 
1. On the Open a pull request page, click **Create pull request**. 
1. Title the pull request: **Add deployment workflow**.

I'll wait for you to create the pull request and respond there. 