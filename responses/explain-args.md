By filling in the `args` field, you're passing arguments to the action, which is running in a Docker container. 

In this case, we passed in arguments with the `-e` option. This allows us to set environment variables in Zeit Now. 

When an action runs, some [environment variables are set by GitHub](https://developer.github.com/actions/creating-github-actions/accessing-the-runtime-environment/#environment-variables) and available in the runtime environment. Although these are available in the Docker container, they need to be explicitly passed to Zeit Now if we want our deployed application to make use of them. 

If you examine our newly deployed app, you'll now see that it looks something like this:

![screenshot of deployed web app with confetti](https://user-images.githubusercontent.com/16547949/52747405-b1c97e80-2fb1-11e9-924c-70fb3a37ce14.png)

By now, you must be getting pretty tired of digging into the Actions tab to get the deployment URL. Let's use another feature of the Zeit Now action: [alias](https://zeit.co/docs/v1/features/aliases).

### :keyboard: Activity: Chain actions in a workflow

1. Click on the **Files changed** tab of this pull request.
1. Click on the pencil to edit the `main.workflow` file.
1. On the side bar, select your deployment workflow.
1. Drag the connector from the deployment action block to the outlined action block for a new action
1. In the Choose action field, type `actions/zeit-now@master` once again
1. Click **Use**
1. In the label field, type `alias`
1. In the :lock: secrets section, check `ZEIT_TOKEN`.
1. Click **Done**.
1. Click **Start commit** on the top right.
1. Enter a commit message.
1. Select **Commit directly to** your branch.
1. Click **Commit changes**

<hr>
<h3 align="center">I'll respond when I detect a new commit on this branch.</h3>
