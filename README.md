# 🧙‍Lambda Layer: Latest AWS SDK 🧙‍

Use the latest AWS-SDK in your Lambda functions with no need to package up in `node_modules`.

## Backstory

Had an issue the other day where I wanted to use `apigatewaymanagementapi` from `AWS-SDK` node library. The specific API was introduced in a fairly recent (few months old) `AWS-SDK` release, but wasn’t available on Lambda, which is [currenty packaged with `AWS-SDK 2.290.0` in the runtime](https://docs.aws.amazon.com/lambda/latest/dg/lambda-runtimes.html).

I therefore needed to bundle a different version of `AWS-SDK` in my `node_modules`, zip it up, and deploy to Lambda every time I wanted to update the function. This got tiresome.

Hence this Lambda Layer. Using `AWS-SDK 2.443.0`

## How to use

The easiest way would be to simply include `arn:aws:lambda:us-east-1:510875216808:layer:latestAWSSDKLayer:1` in your lambda function

If you want to host yourself on your own Lambda Layers, simply upload the `nodejs.zip` file to a new Lambda Layer and add it in each function you want to use.

## To Maybe Do Soon:

Add simple script that fetches latest SDK daily.
