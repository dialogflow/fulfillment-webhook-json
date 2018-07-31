# Dialogflow Fulfillment Webhook JSON Sample
This sample shows Dialogflow's fulfillment webhook JSON requests and responses for v1 and v2 agents, including Actions on Google-specific responses/requests for rich responses (cards, lists, suggestions, etc.) and event (ask for name, location, sign in, etc.)  as well as platform-agnostic request/response examples.

## Setup Instructions
1. [Sign-up/Login](https://accounts.google.com/SignUp?hl=en) to Google account
2. [Create a Firebase project](https://console.firebase.google.com/)
3. Deploy the `responses` directory with [Firebase hosting](https://firebase.google.com/docs/hosting/):
   + Follow the instructions to [set up and initialize Firebase SDK for Cloud Functions](https://firebase.google.com/docs/functions/get-started#set_up_and_initialize_functions_sdk). Make sure to select the project that you have previously generated in the Actions on Google Console and to reply `N` when asked to overwrite existing files by the Firebase CLI.
   + Run `firebase deploy --only hosting` and take note of the endpoint where the `responses` folder has been published. It should look like `Hosting URL: https://${PROJECTID}.firebaseapp.com`
4. Select the correct JSON file for your Dialogflow fulfillment and take a note of the URL of the file (e.g. `https://${PROJECTID}.firebaseapp.com/v2/ActionsOnGoogle/RichResponses/SimpleResponse.json`)
5. Go to the Dialogflow console and select **Fulfillment** from the left navigation menu.
6. **Enable Webhook** > **URL** to the URL of the JSON file from the previous step, then select **Save**.
7. Go to **Intents** from the left navigation menu and for every intent that you'd like to enable fulfillment for:
    + Select the intent
    + In **Fulfillment** > **Enable Webhook** call for this intent.

## Issues & References
* For bugs, please add an issue on [Github](https://github.com/dialogflow/fulfillment-webhook-json/issues).
* Questions? Try [StackOverflow](https://stackoverflow.com/questions/tagged/dialogflow).
* For Dialogflow [documentation](https://docs.dialogflow.com).

## How to Make Contributions?
Please read and follow the steps in the CONTRIBUTING.md

## License
See LICENSE.md

## Terms
Your use of this sample is subject to, and by using or downloading the sample files you agree to comply with, the [Google APIs Terms of Service](https://developers.google.com/terms/) and [Dialogflow's Terms of Use and Privacy Policy](https://api.ai/terms/).
