---
title : "Create access key"
date : "`r Sys.Date()`"
weight : 1
chapter : false
pre : " <b> 2.1 </b> "
---

#### Generate access key

1. Access **IAM**

   - Select **Users**
   - Select **Security credentials**
   - Select **Create access key**

![CodeDeploy](/images/1/0001.png?featherlight=false&width=90pc)

2. Select **Download .csv file** and select **Close**. **Access key** is used to configure terminal local computers or **EC2** to use CLI.

![CodeDeploy](/images/1/0002.png?featherlight=false&width=90pc)

3. Perform CLI configuration. Use the command **```aws configure```**

![CodeDeploy](/images/1/0003.png?featherlight=false&width=90pc)