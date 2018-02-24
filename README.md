# Dialogflow Fulfillment Webhook JSON Sample
This sample shows Dialogflow's fulfillment webhook JSON requests and responses for v1 and v2 agents, including Actions on Google-specific responses/requests for rich responses (cards, lists, suggestions, etc.) and event (ask for name, location, sign in, etc.)  as well as platform-agnostic request/response examples.

## Setup Instructions
1. [Create a Google account](https://accounts.google.com/SignUp?hl=en) and login
1. [Create a Firebase project](https://console.firebase.google.com/)
1. Deploy the `responses` folder with [Firebase hosting](https://firebase.google.com/docs/hosting/):
   1. Follow the instructions to [set up and initialize Firebase SDK for Cloud Functions](https://firebase.google.com/docs/functions/get-started#set_up_and_initialize_functions_sdk). Make sure to select the project that you have previously generated in the Actions on Google Console and to reply `N` when asked to overwrite existing files by the Firebase CLI.
   1. Run `firebase deploy --only hosting` and take note of the endpoint where the `responses` folder has been published. It should look like `Hosting URL: https://${PROJECTID}.firebaseapp.com`
1. Select the correct JSON file for your Dialogflow fulfillment and take a note of the URL of the file (e.g. `https://${PROJECTID}.firebaseapp.com/v2/ActionsOnGoogle/RichResponses/SimpleResponse.json`)
1. Go to the Dialogflow console and select *Fulfillment* from the left navigation menu.
1. Enable *Webhook*, set the value of *URL* to the URL of the JSON file from the previous step, then click *Save*.
1. Select *Intents* from the left navigation menu and for every intent that you'd like to enable fulfillment for:
    1. Select the intent
    1. Click the switch next to `Enable webhook call for this intent` in the fulfillment section

## References and How to report bugs
* If you find any issues, please open a bug here on GitHub
How to make contributions?
Please read and follow the steps in the CONTRIBUTING.md
License
See LICENSE.md
## Terms
Your use of this sample is subject to, and by using or downloading the sample files you agree to comply with, the [Google APIs Terms of Service](https://developers.google.com/terms/) and the [API.AI's Terms of Use and Privacy Policy](https://api.ai/terms/).