---
title : "Tạo service role"
date :  "`r Sys.Date()`" 
weight : 3
chapter : false
pre : " <b> 2.3 </b> "
---

#### Tạo role

1. Truy cập **IAM**

   - Chọn **Roles**
   - Chọn **Create role**

![CodeDeploy](/images/3/0001.png?featherlight=false&width=90pc)

2. Trong giao diện **Select trusted entity**

   - Chọn **AWS service**
   - Chọn **Use case**
   - Chọn **CodeDeploy**
   - Chọn **Next**

![CodeDeploy](/images/3/0002.png?featherlight=false&width=90pc)

3. Chọn **Next**

![CodeDeploy](/images/3/0003.png?featherlight=false&width=90pc)

4. Kiểm tra chi tiết.

- **Role name**, nhập **```CodeDeployServiceRole```**

![CodeDeploy](/images/3/0004.png?featherlight=false&width=90pc)

5. Chọn **Create role**

![CodeDeploy](/images/3/0005.png?featherlight=false&width=90pc)

6. Hoàn thành tạo service role.

![CodeDeploy](/images/3/0006.png?featherlight=false&width=90pc)

