---
layout: single
title:  "srv326 "
header:
  teaser: "unsplash-gallery-image-2-th.jpg"
categories:
  - Jekyll
tags:
  - aws
  - reinvent
  - las vegas

---

Replication - easy to forget
  Code needs replicating,
  Data
  Cloudformation templates. (E.g our build artefacts bucket!)

https://github.com/aws-samples/aws-serverless-workshops

https://53djra61lf.execute-api.eu-west-1.amazonaws.com/prod/health


CognitoIdentityPoolId 	eu-west-1:6d05dc46-b220-486f-b38c-3e19a07085dd 	Cognito Identity Pool Id 	ticket-service-ui-CognitoIdentityPoolId
BucketName 	ticket-service-ui-websitebucket-1n71v6zw1q98d 	The name of the website bucket 	
BucketURL 	http://ticket-service-ui-websitebucket-1n71v6zw1q98d.s3-website-eu-west-1.amazonaws.com 	URL for the static website

d2wrv8xuult0ov.cloudfront.net

Facebook App ID: 293471891279103
Identity pool id: eu-west-1:6d05dc46-b220-486f-b38c-3e19a07085dd

aws s3 sync --acl public-read --delete dist/ s3://ticket-service-ui-websitebucket-1n71v6zw1q98d
