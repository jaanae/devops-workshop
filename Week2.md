# Viikko 2
   
# 1. Create new project

Hint! [Create a project](/create-project.png)


# 2. Creating a batabase
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

2. You can see from the logs that mysql wants us to define a environment variables. So let's do that.
 + **Hint!** [Check the error from here if you can't find it](/error.png)

3. On the left side hand click on Deployment config and click on mysql image. On the upper bar click on Environment.
Now you need add those values, which appeared in the error log.

+ **Hint!** [Check the error from here if you can't find it](/env-properties.png)

# 4. Configuring wordpress application to use mysql database


