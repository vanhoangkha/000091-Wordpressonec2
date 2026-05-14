---
title : "Create instance profile"
date: 2024-01-01
weight : 2
chapter : false
pre : " <b> 2.2 </b> "
---

#### Create instance profile

1. Access **IAM**

   - Select **Policies**
   - Select **Create policy**

![CodeDeploy](/images/2/0001.png?featherlight=false&width=90pc)

2. In the **Create policy** interface, select the **JSON** tab. Then enter the following code:

```
    {
        "Version": "2012-10-17",
        "Statement": [
            {
                "Action": [
                    "s3:Get*",
                    "s3:List*"
                ],
                "Effect": "Allow",
                "Resource": "*"
            }
        ]
    }
```

- Then, select **Next:Tags**

![CodeDeploy](/images/2/0002.png?featherlight=false&width=90pc)

2. Add a key-value tag. Select **Next Review**

![CodeDeploy](/images/2/0003.png?featherlight=false&width=90pc)

3. Check details.

- **Name**, enter **```CodeDeployDemo-EC2-Permissions```**

![CodeDeploy](/images/2/0004.png?featherlight=false&width=90pc)

4. Create a successful policy.

![CodeDeploy](/images/2/0005.png?featherlight=false&width=90pc)

5. In the **IAM** interface

   - Select **Roles**
   - Select **Create role**

![CodeDeploy](/images/2/0006.png?featherlight=false&width=90pc)

6. In the **Select trusted entity** interface

    - Select **AWS service**
    - For **Use case**, select **EC2**
    - Select **Next**

![CodeDeploy](/images/2/0007.png?featherlight=false&width=90pc)

7. Find the newly created policy. Select **Next**

![CodeDeploy](/images/2/0008.png?featherlight=false&width=90pc)

8. Perform a detailed inspection.

- **Role name**, enter **```CodeDeployDemo-EC2-Instance-Profile```**

![CodeDeploy](/images/2/0009.png?featherlight=false&width=90pc)

9. Select **Create role**

![CodeDeploy](/images/2/00010.png?featherlight=false&width=90pc)

10. Create a successful role.

![CodeDeploy](/images/2/00011.png?featherlight=false&width=90pc)

11. Complete the instance profile creation.

![CodeDeploy](/images/2/00012.png?featherlight=false&width=90pc)