---
title : "Create S3 bucket"
date : "`r Sys.Date()`"
weight : 5
chapter : false
pre : " <b> 5. </b> "
---

#### Create S3 bucket

1. Access to **S3**

   - Select **Bucket**
   - Select **Create bucket**

![CodeDeploy](/images/6/0001.png?featherlight=false&width=90pc)

2. In the **Create bucket** interface

- **Bucket name**, enter a unique value. Example: **```codedeploywordpressbucket-2022```**
- Select Region.

![CodeDeploy](/images/6/0002.png?featherlight=false&width=90pc)

3. Select **Create bucket**.

![CodeDeploy](/images/6/0003.png?featherlight=false&width=90pc)

4. Create bucket successfully. Select **View details**

![CodeDeploy](/images/6/0004.png?featherlight=false&width=90pc)

5. Select **Permissions**

![CodeDeploy](/images/6/0005.png?featherlight=false&width=90pc)

6. Scroll down to **Bucket policy**

- Select **Edit**

![CodeDeploy](/images/6/0006.png?featherlight=false&width=90pc)

7. Replace the following policy paragraph:

```
{
    "Version": "2012-10-17",
    "Statement": [
        {
            "Action": [
                "s3:PutObject"
            ],
            "Effect": "Allow",
            "Resource": "arn:aws:s3:::codedeploydemobucket7749/*",
            "Principal": {
                "AWS": [
                    "111122223333"
                ]
            }
        }
    ]
}
```

   - Replace your **Resource ARN**.
   - Change your Account ID.
   - Select **Save changes**

![CodeDeploy](/images/6/0007.png?featherlight=false&width=90pc)

8. Complete the bucket policy configuration.

![CodeDeploy](/images/6/0008.png?featherlight=false&width=90pc)