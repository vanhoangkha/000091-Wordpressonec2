---
title : "Deploy WordPress to an Amazon EC2 instance using CodeDeploy"
date : "`r Sys.Date()`"
weight : 1
chapter : false
---

# Deploy WordPress to an Amazon EC2 instance using CodeDeploy

In this workshop, you deploy WordPress, an open source blogging engine and content management system based on PHP and MySQL, to a single Amazon EC2 running Amazon Linux or Red Hat Enterprise Linux (RHEL).

![CodeDeploy](/images/1/000.png?featherlight=false&width=60pc)

AWS CodeDeploy is a fully managed deployment service that automates software deployment across compute services like Amazon EC2, AWS Fargate, AWS Lambda, and your on-premises servers. AWS CodeDeploy makes it easier to quickly release new features, avoid downtime during application deployment, and make it simpler to update your application. You can use AWS CodeDeploy to automate software deployments and eliminate the need for error-prone manual tasks. The service scales to fit your deployment needs.

#### Content

1. [Introduction](1-introduce/)
2. [Preparation steps](2-prerequiste/)
3. [Launch an EC2 instance](3-connectec2/)
4. [Install CodeDeploy Agent](4-codedeployagent/)
5. [Create S3 bucket](5-creates3bucket/)
6. [Create Deployment Group](6-deployapplication/)
7. [Deploy Application](7-deploywordpress/)
8. [Clean up resource](8-cleanup/)