It's now time to improve the deployment workflow. The first thing we'll do is pass data to our deployment. We can do this using the `args` field, which lets us set arguments for the action.

### :keyboard: Activity: Use environment variables as part of an action

1. [Edit `.github/main.workflow`]({{ url }}) on the master branch.
1. On the side bar, select your deployment workflow.
1. Click **edit** in the zeit-now action.
1. In the **args** field, enter: `-e GITHUB_SHA=$GITHUB_SHA -e GITHUB_ACTOR=$GITHUB_ACTOR`
1. Click **Done**
1. Click **Start commit** on the top right
1. Enter a commit message, select Create a new branch, and click **Commit new file**
1. On the Open a pull request page, click **Create pull request**
1. Title the pull request: **Improve the deployment workflow**

<hr>
<h3 align="center">I'll respond in your new pull request with your next steps.</h3>
