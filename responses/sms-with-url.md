We've now captured the output from the deployment action, although we can't see it. It is stored in a file called `deploy.txt` in the Docker container. We can use the captured deployment URL currently sitting in our runtime environment to include it in the SMS notification.

### :keyboard: Activity: Send a URL with the SMS notification

1. [Edit the `main.workflow` file]({{ url }}) on this branch.
1. On the side bar, select your deployment workflow.
1. Click **edit** in your `sms notify` action.
1. In the **args** field, add a <code>`cat deploy.txt`</code> to the `args` field.
    - Remember that this field previously contained your meesage, so the complete arguments will be:
    ```shell
    $PHONE A deployment just occurred at `cat deploy.txt` check it out
    ```
1. Click **Done**.
1. Click **Start commit** on the top right.
1. Enter a commit message.
1. Select **Commit directly to** your branch.
1. Click **Commit changes**

<hr>
<h3 align="center">I'll respond when I detect a new commit on this branch.</h3>
