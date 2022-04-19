
# Release Notes Automation

## Prerequisites

### Prepare Slack

#### Identify a channel for the Release Notes Automation to update.

Is there an existing channel that Release Notes Automation should post into?  Should a new slack channel be created for Release Notes Automation to update instead?

- Release events should happen infrequently enough that these channel updates will remain informative and not serve as a source of notification fatigue.
- We recommend leveraging a channel that customers are already interfacing with the platform team through, to ensure these updates are available without requiring further steps taken by customer users.


#### Slack Webhook Integration

This workflow requires a Slack app for webhook integration.  More information on Slack webhooks is available here: https://api.slack.com/messaging/webhooks

Slack webhooks can be managed through: https://api.slack.com/apps

Overview of the steps:
- You'll need to create a new app
- select the appropriate slack workspace
- Under `Add features and functionality`, select the `Incoming Webhooks` option
- Enable `Activate incoming webhooks`
- scroll to the bottom of the page and click the `Add new webhook to Workspace` button
- select the channel that the Release Notes Automation should post into and click allow
- a webhook URL is generated that we can now use to create a github repo `SLACK_WEBHOOK` secret with.


### Prepare GitHub

#### Create a repo secret for GitHub Actions

This workflow requires a GitHub Actions repo secret named `SLACK_WEBHOOK`.

More information about what GitHub Action secrets are and how to use them is available here: https://docs.github.com/en/actions/security-guides/encrypted-secrets.


