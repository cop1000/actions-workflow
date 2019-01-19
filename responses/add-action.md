Great work! Since this branch cleanup occurs after pull requests are merged, you'll notice we chose the `pull_request` for the `on` attribute. Most [GitHub events](https://developer.github.com/actions/creating-workflows/workflow-configuration-options/#events-supported-in-workflow-files) are available as triggers.

Let's now add the action block. In the action block we'll specify the branch cleanup action we want to use, and pass any information needed to that action. 

Activity: Use the branch cleanup action

1. Drag the connector to the outlined block for the action.
1. In the Choose action field, type `jessfraz/branch-cleanup-action@master`
1. In the label field, type `branch cleanup`
1. Check the box for :lock: `GITHUB_TOKEN` in the :lock: secrets section. 

I'll respond when you push to this branch.