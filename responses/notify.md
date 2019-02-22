We don't always have to dig into the Actions tab to get the deployment URL, though. One of the best things about defining workflows with GitHub Actions is the ability to use multiple services in a single place to make your life easier. 

Let's practice this by sending yourself an SMS notification when a deployment occurs. You'll need to create an account on Nexmo for this next step. 

### :keyboard: Activity part 1: Get tokens for Nexmo

On Nexmo:
1. [Create an account on Nexmo](https://dashboard.nexmo.com/sign-up), if you don't already have one. You can signup with GitHub if you'd like.
1. Navigate to your [SMS Getting started guide](https://dashboard.nexmo.com/getting-started/#/sms) and jot down each of the following items:
    - API key will be used on GitHub as `NEXMO_API_KEY`
    - API secret will be used on GitHub as `NEXMO_API_SECRET`
1. Navigate to [Numbers](https://dashboard.nexmo.com/your-numbers) section, jot down:
    - The Number assigned to you by Nexmo will be used on GitHub as `NEXMO_NUMBER`


### :keyboard: Activity: Use an action to send an SMS notification on deployment

1. [Edit `.github/main.workflow`]({{ url }}) on this branch.
1. On the side bar, select your deployment workflow.
1. Drag the connector from the deployment action to the new action block.
1. In the Choose action field, type `nexmo-community/nexmo-sms-action@master`
1. Click **Use**
1. In the label field, type `sms notify`
1. In the :lock: secrets section, create new secrets for each of the following fields:
    - `NEXMO_API_KEY`: the API key provided to you by Nexmo
    - `NEXMO_API_SECRET`: the API secret provided to you by Nexmo
    - `NEXMO_NUMBER`: the phone number provided to you by Nexmo
    - `PHONE`: your phone number, the number you wish to notify, preceded by the country code
1. In the **args** field we'll enter the body of the message, I suggest:
    ```
    $PHONE A deployment just occurred check it out
    ```
1. Click **Done**.
1. Click **Start commit** on the top right.
1. Enter a commit message.
1. Select **Commit directly to** your branch.
1. Click **Commit changes**

<hr>
<h3 align="center">I'll respond when I detect a new commit on this branch.</h3>