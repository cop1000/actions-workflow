You should get a notification soon! But it won't include the URL of your deployment. That's because you haven't supplied the Nexmo SMS action with the URL. To do this, we need to save that URL in the deploy action, and access it again in the SMS action. This is possible as a result of the runtime environment that is created when actions run in the Docker container.  

### :keyboard: Activity: Capture the output from an existing action

1. [Edit the `main.workflow` file]({{ url }}) on this branch.
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
