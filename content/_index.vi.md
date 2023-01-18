---
title : "Triển khai WordPress trên EC2 instance sử dụng CodeDeploy"
date : "`r Sys.Date()`"
weight : 1
chapter : false
---

# Triển khai WordPress trên EC2 instance bằng CodeDeploy

Trong workshop này, bạn triển khai WordPress, một công cụ viết blog nguồn mở và hệ thống quản lý nội dung dựa trên PHP và MySQL, cho một  Amazon EC2 duy nhất chạy Amazon Linux hoặc Red Hat Enterprise Linux (RHEL).

![CodeDeploy](/images/1/000.png?featherlight=false&width=60pc)

AWS CodeDeploy là dịch vụ triển khai được quản lý toàn phần có khả năng tự động hóa việc triển khai phần mềm trên các dịch vụ điện toán như Amazon EC2, AWS Fargate, AWS Lambda và các máy chủ chạy tại chỗ của bạn. AWS CodeDeploy giúp bạn nhanh chóng phát hành các tính năng mới một cách dễ dàng hơn, tránh thời gian ngừng hoạt động trong quá trình triển khai ứng dụng và giúp bạn cập nhật ứng dụng đơn giản hơn. Bạn có thể sử dụng AWS CodeDeploy để tự động hóa việc triển khai phần mềm và giúp không cần phải thực hiện các tác vụ thủ công dễ bị lỗi. Dịch vụ thay đổi quy mô để phù hợp với nhu cầu triển khai của bạn.

#### Nội dung

1. [Giới thiệu](1-introduce/)
2. [Các bước chuẩn bị](2-prerequiste/)
3. [Khởi tạo EC2 instance](3-connectec2/)
4. [Cài đặt CodeDeploy Agent](4-codedeployagent/)
5. [Tạo S3 bucket](5-creates3bucket/)
6. [Tạo Deployment Group](6-deployapplication/)
7. [Triển khai ứng dụng](7-deploywordpress/)
8. [Dọn dẹp tài nguyên](8-cleanup/)