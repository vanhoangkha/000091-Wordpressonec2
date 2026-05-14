---
title : "Tạo S3 bucket"
date: 2024-01-01
weight : 5
chapter : false
pre : " <b> 5. </b> "
---

#### Tạo S3 bucket

1. Truy cập vào **S3**

   - Chọn **Bucket**
   - Chọn **Create bucket**

![CodeDeploy](/images/6/0001.png?featherlight=false&width=90pc)

2. Trong giao diện **Create bucket**

- **Bucket name**, nhập giá trị duy nhất. Ví dụ: **```codedeploywordpressbucket-2022```**
- Chọn Region.

![CodeDeploy](/images/6/0002.png?featherlight=false&width=90pc)

3. Chọn **Create bucket**. 

![CodeDeploy](/images/6/0003.png?featherlight=false&width=90pc)

4. Tạo bucket thành công. Chọn **View details**

![CodeDeploy](/images/6/0004.png?featherlight=false&width=90pc)

5. Chọn **Permissions**

![CodeDeploy](/images/6/0005.png?featherlight=false&width=90pc)

6. Kéo xuống đến **Bucket policy**

- Chọn **Edit**

![CodeDeploy](/images/6/0006.png?featherlight=false&width=90pc)

7. Thay đoạn policy sau:

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

   - Thay **Resource ARN** của bạn.
   - Thay Account ID của bạn. 
   - Chọn **Save changes**

![CodeDeploy](/images/6/0007.png?featherlight=false&width=90pc)

8. Hoàn thành cấu hình bucket policy.

![CodeDeploy](/images/6/0008.png?featherlight=false&width=90pc)



