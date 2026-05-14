---
title : "Khởi tạo EC2 instance"
date: 2024-01-01
weight : 3
chapter : false
pre : " <b> 3. </b> "
---

####

1. Khởi tạo EC2 instance.

   - Truy cập vào **EC2**
   - Chọn **Instance**
   - Chọn **Launch instances**

![CodeDeploy](/images/4/0001.png?featherlight=false&width=90pc)

2. Trong giao diện **Launch an instance**

   - **Name and tags**, nhập **```CodeDeployDemo```**
   - Chọn **Quick Start**
   - Chọn **Amazon Linux**

![CodeDeploy](/images/4/0002.png?featherlight=false&width=90pc)

3. Đối với **Instance type** chọn **t3.medium**

   - Chọn **Create new key pair**

![CodeDeploy](/images/4/0003.png?featherlight=false&width=90pc)

4. Đối với **Key pair name**, nhập **```awsstudygroup```**

   - Chọn **Create key pair**
   - Key pair này nên lưu trữ trên máy cẩn thận dùng để SSH vào EC2 instance.

![CodeDeploy](/images/4/0004.png?featherlight=false&width=90pc)

5. Thực hiện cấu hình network

   - VPC: default
   - Subnet: a subnet of VPC default (default is public subnet)
   - Auto-assign public IP: Enable
   - Firewall (security groups): Create security group:
   - SSH / Port 22 / Anywhere
   - HTTP / Port 80 / Anywhere

![CodeDeploy](/images/4/0005.png?featherlight=false&width=90pc)

6. **Advanced details**:

- IAM instance profile: **```CodeDeployDemo-EC2-Instance-Profile```**

![CodeDeploy](/images/4/0006.png?featherlight=false&width=90pc)

7. Hoàn thành tạo EC2 instance.

![CodeDeploy](/images/4/0007.png?featherlight=false&width=90pc)

8. Kiểm tra chi tiết sau 3 phút khởi tạo EC2 instance.

![CodeDeploy](/images/4/0008.png?featherlight=false&width=90pc)

9. Kiểm tra Security của EC2 instance.

![CodeDeploy](/images/4/0009.png?featherlight=false&width=90pc)