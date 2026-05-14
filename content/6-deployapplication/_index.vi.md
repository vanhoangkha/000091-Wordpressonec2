---
title : "Tạo deployment group"
date: 2024-01-01
weight : 6
chapter : false
pre : " <b> 6. </b> "
---

#### Tạo deployment group

1. Cấu trúc file để triển khai:

```
/tmp/
  |--WordPress/
      |-- appspec.yml  
      |-- scripts/
      |    |-- change_permissions.sh
      |    |-- create_test_db.sh
      |    |-- install_dependencies.sh
      |    |-- start_server.sh
      |    |-- stop_server.sh
      |-- wp-admin/
      |    |-- (various files...)
      |-- wp-content/
      |    |-- (various files...)
      |-- wp-includes/
      |    |-- (various files...)
      |-- index.php
      |-- license.txt
      |-- readme.html
      |-- (various files ending with .php...)
```

- Thực hiện tạo application cho CodeDeploy:

```
cd /tmp/WordPress
aws deploy create-application --application-name WordPress_App
```
- Bạn phải cấu hình CLI để sử dụng lệnh.

![CodeDeploy](/images/7/0001.png?featherlight=false&width=90pc)

2. Thực hiện upload revision của CodeDeploy lên Amazon S3.

```
aws deploy push \
  --application-name WordPress_App \
  --s3-location s3://bucketname/WordPressApp.zip \
  --ignore-hidden-files
```

   - Kiểm tra S3 bucket xem kết quả push.

![CodeDeploy](/images/7/0002.png?featherlight=false&width=90pc)

3. Truy cập giao diện **CodeDeploy**

   - Chọn **Applications**
   - Chọn **WordPress_App**

![CodeDeploy](/images/7/0003.png?featherlight=false&width=90pc)

4. Trong giao diện **Applicaiton**

   - Chọn **Deployment groups**
   - Chọn **Create deployment group**

![CodeDeploy](/images/7/0004.png?featherlight=false&width=90pc)

5. Nhập **deployment group name**. Chọn **Service role**.

![CodeDeploy](/images/7/0005.png?featherlight=false&width=90pc)

6. Đối với **Deployment type**

- Chọn **In-place**
- **Environment configuration**, chọn **Amazon EC2 instances**
- Nhập key
- Nhập value.

![CodeDeploy](/images/7/0006.png?featherlight=false&width=90pc)

7. Chọn **Deployment** là **CodeDeployDefault.OneAtATime**

- Chọn **Create deployment group**

![CodeDeploy](/images/7/0007.png?featherlight=false&width=90pc)

8. Tạo deployment group thành công.

![CodeDeploy](/images/7/0008.png?featherlight=false&width=90pc)
