One of the best things about defining workflow with GitHub Actions is the ability to use multiple services in a single place. Let's practice this by sending yourself an SMS notification when a deployment occurs.

We'll let you do this one mostly on your own and we'll check in at the end. First though, you need to create an account on Nexmo and grab the necessary keys.

### :keyboard: Activity part 1: Get tokens for Nexmo

On Zeit:
1. [Create an account on Nexmo](https://dashboard.nexmo.com/sign-up), if you don't already have one. You can signup with GitHub if you'd like.
1. Navigate to your [SMS Getting started guide](https://dashboard.nexmo.com/getting-started/#/sms) and jot down each of the following items:
    - API key will be used on GitHub as `NEXMO_API_KEY`
    - API secret will be used on GitHub as `NEXMO_API_SECRET`
1. Navigate to [Numbers](https://dashboard.nexmo.com/your-numbers) section, jot down:
    - The Number assigned to you by Nexmo will be used on GitHub as `NEXMO_NUMBER`

### :keyboard: Activity: Use an action to send an SMS notification on deployment

1. [Edit `.github/main.workflow`]({{ url }}) on the master branch.
1. On the side bar, select your deployment workflow.
1. Drag the connector from the alias action to the new action block.
1. In the Choose action field, type `nexmo-community/nexmo-sms-action@master`
1. Click **Use**
1. In the label field, type `sms notify`
1. In the :lock: secrets section, create new secrets for each of the following fields:
    - `NEXMO_API_KEY`: the API key provided to you by Nexmo
    - `NEXMO_API_SECRET`: the API secret provided to you by Nexmo
    - `NEXMO_NUMBER`: the phone number provided to you by Nexmo
    - `PHONE`: your phone number, the number you wish to notify
1. In the **args** field we'll enter the body of the message, I suggest:
    ```
    $PHONE A deployment just occurred at https://$GITHUB_SHA.now.sh/ :)
    ```
1. Click **Done**
1. Click **Start commit** on the top right
1. Enter a commit message, select Create a new branch, and click **Commit new file**
1. On the Open a pull request page, click **Create pull request**
1. Title the pull request: `Add deployment notification`

<hr>
<h3 align="center">I'll respond in your new pull request with your next steps.</h3>
