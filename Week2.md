# Viikko 2
   
# 1. Create new project

First try to create project by yourself. If you get stuck check link below.

Hint! [Create a project](/Week1.md)

# 2. Ask Jaana or Eelia to change namespace priviledges

[Slack channel](.slack)

# 2. Creating a batabase image
1. In the upper left corner, click on Developer 
   + **Hint!** [Find a developer view](/Developer-view.png)

2. On the left side hand click on Add                   
   + **Hint!** [Find a Add](/Add.png)

3. Select Container image                               
   + **Hint!** [Find a Container image](/Container-image.png)

4. Next type mysql in the field, select Deployment config and at the bottom click on create.
   + **Hint!** [Check how to fill the container-image](/Developertool-mysql-create.png)

# 3. Create Wordpress image
   * Repeat steps 2 again and now pull the Wordpress image.

# 4. Images
Now let's check if our image is under Deployment Config.

<img src="https://raw.githubusercontent.com/jaanae/devops-workshop/master/images.png" width="60%" height="60%">

If you click on deployment name you will seee that out applications is not running. This is OK for now. Let's envestigate where there is an error.

<img src="https://raw.githubusercontent.com/jaanae/devops-workshop/master/error.png" width="60%" height="60%">

# 5. Investigating a log

1. Each pod has its own log. We get to see it when we select that Pod and click on Log.
<img src="https://raw.githubusercontent.com/jaanae/devops-workshop/master/pod.png" width="60%" height="60%">
<img src="https://raw.githubusercontent.com/jaanae/devops-workshop/master/select-logs.png" width="60%" height="60%">

2. You can see from the log that mysql wants us to define a environment variables. So let's do that.
 + **Hint!** [Check the error from here if you can't find it](/logs.png)

3. On the left side hand click on Deployment config and click on mysql image. On the upper bar click on Environment.
Now you need add those values, which appeared in the error log.

+ **Hint!** [Check the environment variables from here if you can't find it](/env-properties.png)

**You can choose your own values.**

# 6. Configuring wordpress application to use mysql database

We also need to define following environment properties to wordpress images.
The properties need to match with mysql values. 

+ WORDPRESS_DB_HOST = **mysql**
+ WORDPRESS_DB_USER = MYSQL_USERNAME
+ WORDPRESS_DB_PASSWORD = MYSQL_ROOT_PASSWORD
+ WORDPRESS_DB_NAME = MYSQL_DATABASE

+ **Hint!** [Check the environment variables from here](/env-properties-wordpres.png)

# 7. Create mysql database

1. Click on the left side hand Pods.
2. Click on mysql pod 
3. Select Terminal 
4. Login to mysql server by adding this command: **mysql -u user -p 
   * Password is the one that you added in step 6 (MYSQL_ROOT_PASSWORD)
5. Check databases (DB) that you already have by using this command: **SHOW DATABASES;**
6. Now create a new DB by adding this command: **CREATE TABLE {**MYSQL_DATABASE**};**
7. You can check now that DB was created by using this command: **SHOW DATABASES;**

# 8. Check route
1. On the left side hand click on Networks and then Routes. 
2. Click on the link. It will take you to the installation site. 

# 9. Configure Wordpress application

1. Select language (English)
2. Fill the username, password and DB name.

Congratulations Week 2 is now complited. Great Job!


