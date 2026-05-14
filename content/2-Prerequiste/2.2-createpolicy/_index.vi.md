---
title : "Tạo instance profile"
date: 2024-01-01
weight : 2
chapter : false
pre : " <b> 2.2 </b> "
---

#### Tạo instance profile

1. Truy cập **IAM**

   - Chọn **Policies**
   - Chọn **Cretae policy**

![CodeDeploy](/images/2/0001.png?featherlight=false&width=90pc)

2. Trong giao diện **Create policy**, chọn tab **JSON**. Sau đó, điền đoạn code sau:

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

- Sau đó, chọn **Next:Tags**

![CodeDeploy](/images/2/0002.png?featherlight=false&width=90pc)

2. Thêm tag dạng key-value. Chọn **Next Review**

![CodeDeploy](/images/2/0003.png?featherlight=false&width=90pc)

3. Kiểm tra chi tiết. 

- **Name**, nhập **```CodeDeployDemo-EC2-Permissions```**

![CodeDeploy](/images/2/0004.png?featherlight=false&width=90pc)

4. Tạo policy thành công.

![CodeDeploy](/images/2/0005.png?featherlight=false&width=90pc)

5. Trong giao diện **IAM**

   - Chọn **Roles**
   - Chọn **Create role**

![CodeDeploy](/images/2/0006.png?featherlight=false&width=90pc)

6. Trong giao diện **Select trusted entity**

    - Chọn **AWS service**
    - Đối với **Use case**, chọn **EC2**
    - Chọn **Next**

![CodeDeploy](/images/2/0007.png?featherlight=false&width=90pc)

7. Tìm policy vừa tạo. Chọn **Next**

![CodeDeploy](/images/2/0008.png?featherlight=false&width=90pc)

8. Thực hiện kiểm tra chi tiết. 

- **Role name**, nhập **```CodeDeployDemo-EC2-Instance-Profile```**

![CodeDeploy](/images/2/0009.png?featherlight=false&width=90pc)

9. Chọn **Create role**

![CodeDeploy](/images/2/00010.png?featherlight=false&width=90pc)

10. Tạo role thành công.

![CodeDeploy](/images/2/00011.png?featherlight=false&width=90pc)

11. Hoàn thành tạo instance profile.

![CodeDeploy](/images/2/00012.png?featherlight=false&width=90pc)

