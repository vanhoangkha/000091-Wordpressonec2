---
title : "Cài đặt CodeDeploy Agent"
date :  "`r Sys.Date()`" 
weight : 4
chapter : false
pre : " <b> 4. </b> "
---

#### Cài đặt CodeDeploy Agent

1. Thực hiện SSH vào **EC2**

![CodeDeploy](/images/5/0001.png?featherlight=false&width=90pc)

2. Sau đó, cài đặt CodeDeploy Agent

```
sudo yum update -y
sudo yum install ruby -y
sudo yum install wget -y
/opt/codedeploy-agent/bin/codedeploy-agent stop
sudo yum erase codedeploy-agent -y
cd /home/ec2-user/
wget https://bucket-name.s3.region-identifier.amazonaws.com/latest/install
chmod +x ./install
sudo ./install auto
```

- Đối với **bucket name**: là tên của Amazon S3 bucket gồm các file CodeDeploy Resource Kit.
- region-identifier: ví dụ như sau

```
wget https://aws-codedeploy-ap-southeast-1.s3.ap-southeast-1.amazonaws.com/latest/install
```

![CodeDeploy](/images/5/0002.png?featherlight=false&width=90pc)

3. Kiểm tra service đang chạy, sử dụng lệnh sau:

```
sudo service codedeploy-agent status
```
- Nếu như service gặp lỗi hoặc không chạy, sử dụng lệnh sau để khởi động service:

```
sudo service codedeploy-agent start
sudo service codedeploy-agent status
```

![CodeDeploy](/images/5/0003.png?featherlight=false&width=90pc)

4. Thực hiện di chuyển đến thư mục **tmp**

```
cd /tmp
ls
```

![CodeDeploy](/images/5/0004.png?featherlight=false&width=90pc)

5. Cài đặt git để clone resource về:

```
sudo yum install git
```

![CodeDeploy](/images/5/0005.png?featherlight=false&width=90pc)

6. Bạn sẽ thực hiện clone nguồn WordPress.

```
git clone https://github.com/AWS-First-Cloud-Journey/WordPress
```

![CodeDeploy](/images/5/0006.png?featherlight=false&width=90pc)

7. Sau khi clone resource WordPress

- Bạn thực hiện di chuyển đến thư mục:

```
ls
cd WordPress
ls
cat appspec.yml
```
- Bạn cũng xem nội dung của appspec.yml cấu hình lifecycle deploy.

![CodeDeploy](/images/5/0007.png?featherlight=false&width=90pc)

8. Thực hiện clone các file script trong cấu hình file appspec.yml

```
git clone https://github.com/AWS-First-Cloud-Journey/scripts
```

![CodeDeploy](/images/5/0008.png?featherlight=false&width=90pc)



