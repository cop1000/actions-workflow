Great! You successfully added the Zeit Now action to your workflow.

This action will fail since it requires a token for Zeit Now, our deployment provider.

### Get a token for your Zeit

On Zeit:
1. [Create an account on Zeit](https://zeit.co/signup?next=%2Fdashboard), if you don't already have one. You can signup with GitHub if you'd like. 
1. Navigate to your [Tokens](https://zeit.co/account/tokens).
1. Click **Create** to generate a new token for your Zeit account.
1. Name the token something you'll recognize, like "GitHub Actions"
1. Click **Create token**.
1. Click on **Reveal** next to the new token, and copy it to your clipboard. 

### Securely store your token in your GitHub repository

In your open pull request on GitHub:
1. Click on the **Files changed** tab of this pull request.
1. Click on the pencil to edit the `main.workflow` file. 
1. In the `deploy` action block, click on **Edit**.
1. Drag the connector from the workflow block to the outlined action block for the action.
1. In the :lock: secrets section click on **Enter value** next to next to :lock: `ZEIT_TOKEN`.
1. Paste your token from Zeit.
1. Click **Add secret**
1. Click **Done**.
1. Click **Start commit** on the top right. 
1. Enter a commit message.
1. Select **Commit directly to** your branch.
1. Click **Commit changes**

I'll wait for you to push to this branch before responding. 