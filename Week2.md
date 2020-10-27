# Viikko 2
   
# 1. Create new project

First try to create a project by yourself. If you get stuck, check the link below.

Hint! [Create a project](/Week1.md)

# 2. Ask the instructors to change your namespace priviledges

- The mysql container image that this exercise uses, is built to use the user ID 999. Namespaces/projects with default privileges cannot run containers as users below the ID of 10000. The instructors will change the allowed users ID's to run containers in your namespace from the default value of 1000620000/10000 to 0/10000. This change is needed to run the mysql container as the mysql default user ID 999.
- [Slack channel](.slack)

- When your namespace has new priviledges, proceed to the next step.

# 2. Creating a batabase image
1. In the upper left corner, click on Administrator and choose Developer. 
   + **Hint!** [Find a developer view](/Developer-view.png)

2. On the left hand side click on Add.
   + **Hint!** [Find a Add](/Add.png)

3. Select Container image.                     
   + **Hint!** [Find a Container image](/Container-image.png)

4. Next type mysql in the field, select Deployment config and at the bottom and then click create.
   + **Hint!** [Check how to fill the container-image](/Developertool-mysql-create.png)

# 3. Create Wordpress image
   * Repeat the steps 1-4 under **2. Creating a database image** again and now pull the Wordpress image.

# 4. Images
Now let's check if our image is under Deployment Configs.
Return back to the Administrator view and click **Workloads > deployment configs** on the left hand side.

<img src="https://raw.githubusercontent.com/jaanae/devops-workshop/master/images.png" width="60%" height="60%">

If you click on deployment name you will see that our application is not running. This is OK for now. Let's investigate whether there are any errors.

<img src="https://raw.githubusercontent.com/jaanae/devops-workshop/master/error.png" width="60%" height="60%">

# 5. Investigating a log

**First problem:**

1. First navigate to the **deployment configs** and click on mysql.
2. Click on YAML.
3. Find securityContext key.
4. Add the following line under it: 
      runAsUser: 999
 
 This will force the container to run as user ID 999 which is the default user ID for mysql. Mysql can also be run as different user IDs but that would require modifying the container which we will leave for another course. How ever if you want to know more about modifying containerized applications you can find more information about it here: https://docs.openshift.com/container-platform/4.4/applications/application_life_cycle_management/odc-editing-applications.html
 
+ **Hint!** [Check the yml file if you get stuck](/deployment-config.yml) 

**Second problem:**

1. Each pod has its own log. We get to see it when we select the Pod and click on Log.
<img src="https://raw.githubusercontent.com/jaanae/devops-workshop/master/pod.png" width="60%" height="60%">
<img src="https://raw.githubusercontent.com/jaanae/devops-workshop/master/select-logs.png" width="60%" height="60%">

2. You can see from the log that mysql wants us to define an environment variables. So let's do that.
 + **Hint!** [Check the error from here if you can't find it](/logs.png)

3. On the left side hand click on Deployment configs and click mysql image. On the upper bar click Environment.
Now you need to add these values as environment variables.

**MYSQL_DATABASE**
**MYSQL_USERNAME**
**MYSQL_ROOT_PASSWORD**

+ **Hint!** [Check the environment variables from here](/env-properties.png)

Environment variables are variable information that is given to the container at startup.

# 6. Configuring wordpress application to use mysql database

We also need to define the following environment variables to the wordpress image.
The variables need to match with the values from your mysql. 

+ WORDPRESS_DB_HOST = **mysql**
+ WORDPRESS_DB_USER = MYSQL_USERNAME
+ WORDPRESS_DB_PASSWORD = MYSQL_ROOT_PASSWORD
+ WORDPRESS_DB_NAME = MYSQL_DATABASE
+ WORDPRESS_DB_PORT = 3306

+ **Hint!** [Check the environment variables from here](/env-properties-wordpres.png)


# 7. Check route
1. On the left side hand click on **Networks > Routes**. 
2. Click on the wordpress link in the Location column. It will take you to the ready wordpress application. 

# 8. Configure Wordpress application

1. Select language (English)
2. Fill the username, password and DB name.
- **Try to not leave the application running without setting the username and password first. The wordpress is open to the internet and as long as there is no password set, anyone in the world can set the username and password and take control of your wordpress to do what ever evil things they want.**


Congratulations! Week 2 is now completed. Great Job!


