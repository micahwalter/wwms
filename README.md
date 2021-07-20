# wwms

Conserving What Would Micah Say

## Overview

This is a serverless incarnation of a special API method at [Cooper Hewitt, Smithsonian Design Museum](https://www.cooperhewitt.org) called "[What would Micah say?](https://collection.cooperhewitt.org/api/methods/cooperhewitt.labs.whatWouldMicahSay)" At the time of this writing, the API method still exists and you should go an use it there if you want it. However, things change, and I wanted to conserve the method and it's output long term. It's now available freely right [here](https://api.micahwalter.com/wwms).

You can also try out this method right on my website by going to [here](https://www.micahwalter.com/wwms).

## Serverless Stuff

This repo is designed to be easily deployable to [AWS](https://aws.amazon.com). It uses a [Serverless Application Model](https://aws.amazon.com/serverless/sam/) or "SAM" for deployment, which makes it super easy to test locally and deploy and deploy al the parts to your own AWS account.

To get started you will need to install the [SAM CLI](https://docs.aws.amazon.com/serverless-application-model/latest/developerguide/serverless-sam-cli-install.html) for your operating system. This assumes you have an AWS account and credentials configured on your system.

Once you have SAM set up for your system and account you can test locally and deploy to your account.

## Test Locally

To test the Lambda function locally you will need [Docker](https://docs.docker.com/get-docker/) installed on your system. Once you have Docker installed and running all you need to do are the following two commands:

    > sam build
    > sam local start-api

Once you have the api up and running you should be able to go to `http://127.0.0.1:3000/` and see the response in your browser.

## Deploy to AWS

To deploy to AWS all you need to do the first time is the following command:

    > sam deploy --guided

SAM will create a Cloud Formation template and build out the resources for you. Once it is done doing its thing you will receive a URL for the live API.
