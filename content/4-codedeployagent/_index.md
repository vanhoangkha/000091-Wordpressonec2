---
title : "Installing CodeDeploy Agent"
date: 2024-01-01
weight : 4
chapter : false
pre : " <b> 4. </b> "
---

#### Install CodeDeploy Agent

1. Do SSH into **EC2**

![CodeDeploy](/images/5/0001.png?featherlight=false&width=90pc)

2. Then install CodeDeploy Agent

```
sudo yum update -y
sudo yum install ruby ​​-y
sudo yum install wget -y
/opt/codedeploy-agent/bin/codedeploy-agent stop
sudo yum erase codedeploy-agent -y
cd /home/ec2-user/
wget https://bucket-name.s3.region-identifier.amazonaws.com/latest/install
chmod +x ./install
sudo ./install auto
```

- For **bucket name**: is the name of Amazon S3 bucket including CodeDeploy Resource Kit files.
- region-identifier: example as follows

```
wget https://aws-codedeploy-ap-southeast-1.s3.ap-southeast-1.amazonaws.com/latest/install
```

![CodeDeploy](/images/5/0002.png?featherlight=false&width=90pc)

3. Check the service is running, use the following command:

```
sudo service codedeploy-agent status
```
- If the service has an error or is not running, use the following command to start the service:

```
sudo service codedeploy-agent start
sudo service codedeploy-agent status
```

![CodeDeploy](/images/5/0003.png?featherlight=false&width=90pc)

4. Make a move to the **tmp** folder

```
cd /tmp
ls
```

![CodeDeploy](/images/5/0004.png?featherlight=false&width=90pc)

5. Install git to clone resources to:

```
sudo yum install git
```

![CodeDeploy](/images/5/0005.png?featherlight=false&width=90pc)

6. You will perform a clone of the WordPress source.

```
git clone https://github.com/AWS-First-Cloud-Journey/WordPress
```

![CodeDeploy](/images/5/0006.png?featherlight=false&width=90pc)

7. After cloning the WordPress resource

- You make the move to the directory:

```
ls
WordPress cd
ls
cat appspec.yml
```
- You also see the contents of the appspec.yml lifecycle deploy configuration.

![CodeDeploy](/images/5/0007.png?featherlight=false&width=90pc)

8. Do clone script files in appspec.yml . configuration file

```
git clone https://github.com/AWS-First-Cloud-Journey/scripts
```

![CodeDeploy](/images/5/0008.png?featherlight=false&width=90pc)