We can't see it, but we've captured the output from the deployment action, which gives us the deployment URL. Let's now use it to alias that URL.

### :keyboard: Activity: Alias the deployment

1. Click on the **Files changed** tab of this pull request.
1. Click on the pencil to edit the `main.workflow` file.
1. On the side bar, select your deployment workflow.
1. Click **edit** in your alias action.
1. In the **args** field, add `\`cat deploy.txt\` $GITHUB_SHA`.
    - Remember that this field previously contained `alias`, so the complete arguments will be: `alias \`cat deploy.txt\` $GITHUB_SHA`
1. Click **Done**.
1. Click **Start commit** on the top right.
1. Enter a commit message.
1. Select **Commit directly to** your branch.
1. Click **Commit changes**

<hr>
<h3 align="center">I'll respond when I detect a new commit on this branch.</h3>
