
---
title : "Triển khai ứng dụng WordPress"
date: 2024-01-01
weight : 7
chapter : false
pre : " <b> 7. </b> "
---
#### Triển khai ứng dụng WordPress

1. Quay lại giao diện application

   - Chọn **Revisions**
   - Chọn **Deploy application**

![CodeDeploy](/images/7/0009.png?featherlight=false&width=90pc)

2. Trong giao diện deployment

   - Chọn deployment group đã tạo.
   - Chọn **My application is stored in Amazon S3**
   - Còn lại cấu hình mặc định.

![CodeDeploy](/images/7/00010.png?featherlight=false&width=90pc)

3. Chọn **Create deployment**

![CodeDeploy](/images/7/00011.png?featherlight=false&width=90pc)

4. Deployment thành công.

![CodeDeploy](/images/7/00012.png?featherlight=false&width=90pc)

5. Xem chi tiết event deployment.

![CodeDeploy](/images/7/00013.png?featherlight=false&width=90pc)

6. Xem deployment history về deployment đã thành công.

![CodeDeploy](/images/7/00014.png?featherlight=false&width=90pc)

7. Xem deployment group đã deploy thành không.

![CodeDeploy](/images/7/00015.png?featherlight=false&width=90pc)

8.  Xem application deploy thành công.

![CodeDeploy](/images/7/00016.png?featherlight=false&width=90pc)

9. Kiểm tra bằng cách truy cập vào ứng dụng WordPress bằng Public Ipv4 DNS.

![CodeDeploy](/images/7/00017.png?featherlight=false&width=90pc)

10. Thành công với trang Apache

![CodeDeploy](/images/7/00018.png?featherlight=false&width=90pc)

11. Thực hiện điều hướng đến WordPress.

![CodeDeploy](/images/7/00019.png?featherlight=false&width=90pc)

12. Thực hiện cấu hình WordPress.

![CodeDeploy](/images/7/00020.png?featherlight=false&width=90pc)

13. Cấu hình WordPress

    - **Database name**: test.
    - **Username**: root
    - **Password**: để trống
    - **Database Host**: localhost
    - **Table Prefix**: wp_
    - Chọn **Submit**

![CodeDeploy](/images/7/00021.png?featherlight=false&width=90pc)

14. Chọn **Run the installation**

![CodeDeploy](/images/7/00022.png?featherlight=false&width=90pc)

15. Hoàn thành các thông tin.

![CodeDeploy](/images/7/00023.png?featherlight=false&width=90pc)

16. Giao diện WordPress.

![CodeDeploy](/images/7/00024.png?featherlight=false&width=90pc)