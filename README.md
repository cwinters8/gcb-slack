# Google Cloud Build Slack notifiers

This repository houses the functions that trigger a Slack webhook based on Google Cloud Build events.

## Prerequisites
The prerequisites and full instructions for getting this set up can be found here: https://cloud.google.com/cloud-build/docs/configure-third-party-notifications

## Function Deployment
To deploy one of these functions, navigate to the appropriate directory for the app and environment. We'll use hso-dev (Horse Sales Online development environment) for this example.
```bash
cd hso-dev
```

Then run the command to deploy the function, replacing the webhook URL with the appropriate one from Slack
```bash
gcloud functions deploy subscribeSlack --trigger-topic cloud-builds --runtime nodejs10 --set-env-vars "SLACK_WEBHOOK_URL=https://hooks.slack.com/services/..."
```