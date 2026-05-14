---
title : "Deploy the WordPress App"
date: 2024-01-01
weight : 7
chapter : false
pre : " <b> 7. </b> "
---
#### Deploy WordPress App

1. Back to the application interface

   - Select **Revisions**
   - Select **Deploy application**

![CodeDeploy](/images/7/0009.png?featherlight=false&width=90pc)

2. In the deployment interface

   - Select the created deployment group.
   - Select **My application is stored in Amazon S3**
   - Remaining default configuration.

![CodeDeploy](/images/7/00010.png?featherlight=false&width=90pc)

3. Select **Create deployment**

![CodeDeploy](/images/7/00011.png?featherlight=false&width=90pc)

4. Deployment is successful.

![CodeDeploy](/images/7/00012.png?featherlight=false&width=90pc)

5. View event deployment details.

![CodeDeploy](/images/7/00013.png?featherlight=false&width=90pc)

6. View the deployment history of the successful deployment.

![CodeDeploy](/images/7/00014.png?featherlight=false&width=90pc)

7. See if the deployment group has deployed to zero.

![CodeDeploy](/images/7/00015.png?featherlight=false&width=90pc)

8. See the application deploy successfully.

![CodeDeploy](/images/7/00016.png?featherlight=false&width=90pc)

9. Test by accessing the WordPress application using Public Ipv4 DNS.

![CodeDeploy](/images/7/00017.png?featherlight=false&width=90pc)

10. Success with Apache Sites

![CodeDeploy](/images/7/00018.png?featherlight=false&width=90pc)

11. Make a navigation to WordPress.

![CodeDeploy](/images/7/00019.png?featherlight=false&width=90pc)

12. Perform WordPress configuration.

![CodeDeploy](/images/7/00020.png?featherlight=false&width=90pc)

13. WordPress Configuration

    - **Database name**: test.
    - **Username**: root
    - **Password**: leave blank
    - **Database Host**: localhost
    - **Table Prefix**: wp_
    - Select **Submit**

![CodeDeploy](/images/7/00021.png?featherlight=false&width=90pc)

14. Select **Run the installation**

![CodeDeploy](/images/7/00022.png?featherlight=false&width=90pc)

15. Complete the information.

![CodeDeploy](/images/7/00023.png?featherlight=false&width=90pc)

16. WordPress theme.

![CodeDeploy](/images/7/00024.png?featherlight=false&width=90pc)