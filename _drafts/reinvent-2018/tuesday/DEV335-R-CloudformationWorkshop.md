---
layout: single
title:  "DEV335: Hands0On with advanced AWS CloudFormation Techniques and new features."
header:
  teaser: "unsplash-gallery-image-2-th.jpg"
categories:
  - Jekyll
tags:
  - aws
  - reinvent
  - las vegas
  - CloudFormation
---

### Credit
Eric Z. Beard, Jonathan Cornell, Erin McGill
AWS Partner Solutions Architects

Julio Lins and Diwakar Chakravarthy
AWS Software Development Engineers.

4 Labs
1. Custom resources

Template has a custom resource. Sends a request to the specified service token *must be same region
Custom code that runs on stack creation, updates or deletion.
Signal success or failure by pre-signed s3 url.

https://github.com/aws-samples/aws-cloudformation-advanced-reinvent-2018

You can extend the capabilities of CloudFormation with custom resources by delegating work to a Lambda function that is specially crafted to interact with the CloudFormation service. In your code, you implement the create, update, and delete actions, and then you send a response with the status of the operation.

In this lab, you will create a custom resource that generates an SSH key and stores it in SSM parameter store.

Function ARN: arn:aws:lambda:us-east-1:110642024509:function:ssh-key-gen

Different types for params in CloudFormation look useful, e.g       Type: AWS::EC2::VPC::Id


The following sample data shows what AWS CloudFormation includes in a request to a lambda for processing a custom resources:

{
   "RequestType" : "Create",
   "ResponseURL" : "http://pre-signed-S3-url-for-response",
   "StackId" : "arn:aws:cloudformation:us-west-2:123456789012:stack/stack-name/guid",
   "RequestId" : "unique id for this create request",
   "ResourceType" : "Custom::TestResource",
   "LogicalResourceId" : "MyTestResource",
   "ResourceProperties" : {
      "Name" : "Value",
      "List" : [ "1", "2", "3" ]
   }
}

In the response, the custom resource provider can also include name-value pairs that the template developer can access. For example, the response can include output data if the request succeeded or an error message if the request failed. For more information about responses, see Custom Resource Response Objects.



2. Macros

ARN:  arn:aws:lambda:us-east-1:110642024509:function:ssh-key-gen-macro

    Type: AWS::CloudFormation::Macro

Question: Validation, e.g using the CLI?
Question: How do I see it in the console?


3. Mappings and Stack sets
4. Drift Detection
