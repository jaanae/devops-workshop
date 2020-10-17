# Viikko 2
   
# 1. Create new project

<img src="https://raw.githubusercontent.com/jaanae/devops-workshop/master/create-project.png" width="60%" height="60%">


# 2. Creating a batabase
1. In the upper left corner, click on Developer
<img src="https://raw.githubusercontent.com/jaanae/devops-workshop/master/Developer-view.png" width="40%" height="40%">

2. On the left side hand click on Add
<img src="https://raw.githubusercontent.com/jaanae/devops-workshop/master/Add.png" width="40%" height="40%">

3. Select Container image
<img src="https://raw.githubusercontent.com/jaanae/devops-workshop/master/Container-image.png" width="60%" height="60%">

4. Next type mysql in the field, select Deployment config and at the bottom click on create.
<img src="https://raw.githubusercontent.com/jaanae/devops-workshop/master/Developertool-mysql-create.png" width="60%" height="60%">

# 3. Create Wordpress image
   * Repeat steps 2 again and now pull the Wordpress image.

# 4. Images
Now let's check if our image is under Deployment Config.

<img src="https://raw.githubusercontent.com/jaanae/devops-workshop/master/images.png" width="60%" height="60%">

You may have already noticed that when you click on the Pod then the image will look red. This is OK. Let's envestigate where there is an error.

<img src="https://raw.githubusercontent.com/jaanae/devops-workshop/master/error.png" width="60%" height="60%">

Each pod has its own logs. We get to see it when we select that Pod and click on Log.
<img src="https://raw.githubusercontent.com/jaanae/devops-workshop/master/pod.png" width="60%" height="60%">
<img src="https://raw.githubusercontent.com/jaanae/devops-workshop/master/select-logs.png" width="60%" height="60%">

# 4. Configuring wordpress application to use mysql database


