# Beaverbot
Beaverbot is an automation tool for logging on-the-job hours in [SmartAssessor](https://www.smartassessor.co.uk/)

> It's called beaverbot because it does the logging

To automate logging your own hours, you can fork this repo to use the GitHub action, or clone it to run it locally.

## Using GitHub Actions
You'll have to add your SmartAssessor username and password as secrets for the workflow to run successfully:

In your own fork of the repo, go to `Settings` > `Secrets & Variables` > `Actions`

Select `New Repository Secret`, and add:

USERNAME (your SmartAssessor username)
PASSWORD (your SmartAssessor password)

## Running locally
If you want to run the program locally, you'll need to add a `.env` to the root of the directory, containing:

USERNAME (your SmartAssessor username)
PASSWORD (your SmartAssessor password)

## Logging your hours
Update `data.json` with your on the job day/hour entries for the week, and either:

- Commit your changes and manually trigger the GitHub Action to log your on the job hours.

OR

- Run `npx playwright test` to log your on the job hours.

> Please note: the process will fail if an entry is duplicated, so you may have to go in and edit entries manually