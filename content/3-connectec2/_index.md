---
title : "Launch an EC2 instance"
date: 2024-01-01
weight : 3
chapter : false
pre : " <b> 3. </b> "
---

####

1. Launch an EC2 instance.

   - Access to **EC2**
   - Select **Instance**
   - Select **Launch instances**

![CodeDeploy](/images/4/0001.png?featherlight=false&width=90pc)

2. In the **Launch an instance** interface

   - **Name and tags**, enter **```CodeDeployDemo```**
   - Select **Quick Start**
   - Select **Amazon Linux**

![CodeDeploy](/images/4/0002.png?featherlight=false&width=90pc)

3. For **Instance type** select **t3.medium**

   - Select **Create new key pair**

![CodeDeploy](/images/4/0003.png?featherlight=false&width=90pc)

4. For **Key pair name**, enter **```awsstudygroup```**

   - Select **Create key pair**
   - This key pair should be stored on the machine carefully to SSH into the EC2 instance.

![CodeDeploy](/images/4/0004.png?featherlight=false&width=90pc)

5. Perform network configuration

   - VPC: Default
   - Subnet: a subnet of VPC default (default is public subnet)
   - Auto-assign public IP: Enable
   - Firewall (security groups): Create security group:
   - SSH / Port 22 / Anywhere
   - HTTP / Port 80 / Anywhere

![CodeDeploy](/images/4/0005.png?featherlight=false&width=90pc)

6. **Advanced details**:

- IAM instance profile: **```CodeDeployDemo-EC2-Instance-Profile```**

![CodeDeploy](/images/4/0006.png?featherlight=false&width=90pc)

7. Complete EC2 instance creation.

![CodeDeploy](/images/4/0007.png?featherlight=false&width=90pc)

8. Check details after 3 minutes of EC2 instance initialization.

![CodeDeploy](/images/4/0008.png?featherlight=false&width=90pc)

9. Check the Security of the EC2 instance.

![CodeDeploy](/images/4/0009.png?featherlight=false&width=90pc)