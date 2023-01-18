---
title : "Create deployment group"
date : "`r Sys.Date()`"
weight : 6
chapter : false
pre : " <b> 6. </b> "
---

#### Create a deployment group

1. File structure for deployment:

```
/tmp/
  |--WordPress/
      |-- appspec.yml
      |-- scripts/
      | |-- change_permissions.sh
      | |-- create_test_db.sh
      | |-- install_dependencies.sh
      | |-- start_server.sh
      | |-- stop_server.sh
      |-- wp-admin/
      | |-- (variable files...)
      |-- wp-content/
      | |-- (variable files...)
      |-- wp-includes/
      | |-- (variable files...)
      |-- index.php
      |-- license.txt
      |-- readme.html
      |-- (variable files ending with .php...)
```

- Create application for CodeDeploy:

```
cd /tmp/WordPress
aws deploy create-application --application-name WordPress_App
```
- You must configure the CLI to use the command.

![CodeDeploy](/images/7/0001.png?featherlight=false&width=90pc)

2. Upload revisions of CodeDeploy to Amazon S3.

```
aws deploy push \
  --application-name WordPress_App\
  --s3-location s3://bucketname/WordPressApp.zip \
  --ignore-hidden-files
```

   - Check the S3 bucket to see the push results.

![CodeDeploy](/images/7/0002.png?featherlight=false&width=90pc)

3. Access the **CodeDeploy** interface

   - Select **Applications**
   - Select **WordPress_App**

![CodeDeploy](/images/7/0003.png?featherlight=false&width=90pc)

4. In the **Applicaiton** interface

   - Select **Deployment groups**
   - Select **Create deployment group**

![CodeDeploy](/images/7/0004.png?featherlight=false&width=90pc)

5. Enter **deployment group name**. Select **Service role**.

![CodeDeploy](/images/7/0005.png?featherlight=false&width=90pc)

6. For **Deployment type**

- Select **In-place**
- **Environment configuration**, select **Amazon EC2 instances**
- Enter key
- Enter value.

![CodeDeploy](/images/7/0006.png?featherlight=false&width=90pc)

7. Select **Deployment** as **CodeDeployDefault.OneAtATime**

- Select **Create deployment group**

![CodeDeploy](/images/7/0007.png?featherlight=false&width=90pc)

8. Create a successful deployment group.

![CodeDeploy](/images/7/0008.png?featherlight=false&width=90pc)