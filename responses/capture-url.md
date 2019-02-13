The deployment action will succeed, but the alias action will fail. This is because the alias action requires a [source and target url](https://zeit.co/docs/v1/features/aliases/#creating-aliases), which we've not supplied.

When the deployment action runs, you may have noticed that it returns the deployment URL in the log output. We can redirect this output to a file by accessing the Docker container running the action.

### :keyboard: Activity: Capture the output from an existing action

1. Click on the **Files changed** tab of this pull request.
1. Click on the pencil to edit the `main.workflow` file.
1. On the side bar, select your deployment workflow.
1. Click **edit** in your deployment action.
1. In the **args** field, add `deploy > deploy.txt`.
    - Remember that we've previously used this field to pass in the runtime environment variables. You'll want to leave those in place, so the complete arguments will be:
    ```shell
    -e GITHUB_SHA=$GITHUB_SHA -e GITHUB_ACTOR=$GITHUB_ACTOR deploy > deploy.txt
    ```
1. Click **Done**.
1. Click **Start commit** on the top right.
1. Enter a commit message.
1. Select **Commit directly to** your branch.
1. Click **Commit changes**

<hr>
<h3 align="center">I'll respond when I detect a new commit on this branch.</h3>
