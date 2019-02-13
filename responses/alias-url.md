We've now captured the output from the deployment action, although we can't see it. It is stored in a file called `deploy.txt` in the Docker container. We can use the captured deployment URL to alias the deployment. Let's alias it to our commit SHA.

### :keyboard: Activity: Alias the deployment

1. Click on the **Files changed** tab of this pull request.
1. Click on the pencil to edit the `main.workflow` file.
1. On the side bar, select your deployment workflow.
1. Click **edit** in your alias action.
1. In the **args** field, add <code>\`cat deploy.txt\` $GITHUB_SHA</code>.
    - Remember that this field previously contained `alias`, so the complete arguments will be:
    ```shell
    alias `cat deploy.txt` $GITHUB_SHA
    ```
1. Click **Done**.
1. Click **Start commit** on the top right.
1. Enter a commit message.
1. Select **Commit directly to** your branch.
1. Click **Commit changes**

<hr>
<h3 align="center">I'll respond when I detect a new commit on this branch.</h3>
