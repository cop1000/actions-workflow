Great work! Since this branch cleanup occurs after pull requests are merged, you'll notice we chose the `pull_request` for the `on` attribute. Most [GitHub events](https://developer.github.com/actions/creating-workflows/workflow-configuration-options/#events-supported-in-workflow-files) are available as triggers.

Let's now add the action block. In the action block we'll specify the branch cleanup action we want to use, and pass any information needed to that action. 

Activity: Use the branch cleanup action

1. Click on the **Files changed** tab of this pull request.
1. Click on the pencil to edit the `main.workflow` file. 
1. Drag the connector from the workflow block to the outlined action block for the action.
1. In the Choose action field, type `jessfraz/branch-cleanup-action@master`.
1. Click **Use**.
1. In the label field, type `branch cleanup`
1. Check the box for :lock: `GITHUB_TOKEN` in the :lock: secrets section. 
1. Click **Done**.
1. Click **Start commit** on the top right. 
1. Enter a commit message.
1. Select **Commit directly to** your branch.
1. Click **Commit changes**

I'll respond when the commit is created.