# AWS Lambda CloudFormation & CodePipeline

This is a simple template for Creating & deploying a Lambda function using AWS CloudFormation and AWS CodePipeline.


# Files

 - `lambda_function.py`  a simple python script that we want to deploy.
 - `template.yaml` the Cloudformation script to create the lambda function
 - `buildspec.yml` the Buildcode script used in the CodePipeline for the deployment

# Note
Make sure to attache the right policies to the CodePipeline Role to preform the deployment which are:

 - Access to IAM to create Role for Lambda
 - Access to the required S3 Bucket
 - Access to CLoudFormation
 - And access to Labmda Function
 
To create the CodePipeline can follow this doc:
https://docs.aws.amazon.com/codepipeline/latest/userguide/tutorials-serverlessrepo-auto-publish.html
And make sure to add the required environment variable ( `${S3_BUCKET}` ) in CodeBuild Advanced section.

