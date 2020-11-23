## Final week.
So far we have created all the basic components of an OpenShift application except networking.
On this week we will be creating a sample httpd application from it's basic components that includes a pod, persistent storage, service and route.
This is usually not the way that openShift applications are built but we thought that understanding how the basic components of an application work together is really important and in fact understanding the underlying structure makes creating real applications much easier.
The order that the components are made basically does not matter but we will be making them in the following order to minimize temporary error messages.
1. persistent Volume Claim
2. Pod
3. Service
4. Route

- **The parts of this week can be made in the same week2 project that was used on weeks 2 and 3.**

# 1. Creating a Persistent Volume Claim

- first we need to create a PVC so that it is ready for the Pod when we deploy it.
- Create a new PVC with the following info:
  - StorageClass: ibmc-vpc-block-retain-general-purpose
  - name: week4-pvc
  - AccessMode: SingleUser
  - Size: 10 GiB
   + **Hint!** [Check how to create the PVC here](/create-pvc.png)
   + **Hint!** [Check PVC details here](/pvc-details.png)

# 2. Deploying the httpd Pod

- The second task is to create a pod. In this excersize we wont be creating a deployment for this application so we will only create a single pod. This is normally never done like this in production or even development situations but this helps in understanding the basic structure of the application.
- A pod is either a single container or it can contain multiple containers depending on the application that is being run. Usually there are at least two containers at start. One initialization container and then the application running container itself. The init container may for example run some initialization commands inside the application container as it is starting up and when the main container starts, the init container is deleted as it is not needed anymore.
   + **Hint!** [Check how to create the Pod here](/create-pod.png)
   + **Hint!** [Check how to fill in the yaml here](/pod-yaml.png)
- Change the names and namespace names in the example with your pod and namespace names. Also remember to check that the **intendations are correct**, otherwise the pod cannot be created.
- Click **Create** and check that the pod is in running state. The pod initialization can take up to few minutes.
<img src="https://raw.githubusercontent.com/jaanae/devops-workshop/master/pod-running.png" width="60%" height="60%">


# 3. Creating a Service

- Pods have an internal network that is not accessible from anywhere else but from pods themselves. This internal network is used so that multiple pods can easily work togehter. The pods services can be exposed outside of the internal network with services. 
- A service is basically a logical router that maps an external port to a port in the container.
- In earlier weeks the service was automatically created by the deployment that was used.
   + **Hint!** [Check how to create the Service here](/create-svc.png)
   + **Hint!** [Check how to fill in the Service yaml here](/svc-yaml.png)
- Change the names and namespace names in the example with your service and namespace names. Also remember to check that the **intendations are correct**, otherwise the service cannot be created.
- Click **create** and go to the **Pods** tab. Check that the pod you created earlier is visible there. This means that the service is bound to the pod.
<img src="https://raw.githubusercontent.com/jaanae/devops-workshop/master/svc-pods.png" width="60%" height="60%">
   
# 4. creating a Route

- Now when the Service is created, the Pod can be accessed from the OpenShift cluster network. We want to access the pod over internet so we need to expose the service that we just created to internet.
- This can be done by creating a **Route** A Route gives the service an online endpoint where all traffic is routed.
- In earlier weeks the route was automatically created by the deployment that was used.
   + **Hint!** [Check how to create the Route here](/create-route.png)
   + **Hint!** [Check the route details here](/route-details.png)
- The **Hostname** of the route tells the system where to route the traffic. It needs to be in the form: **ServiceName-ProjectName.OpenShiftClusterAddress**
- Click create and on the **Route Overview** page, click the **Location** link. This is what you should see:
<img src="https://raw.githubusercontent.com/jaanae/devops-workshop/master/httpd-page.png" width="60%" height="60%">
- If you get any errors or a message that says "Application not found" check that the route **HostName** is correct.

# 5. Confirming the application

- Now that the application is up and running, we confirmed that it works by clicking the route link and seeing the httpd welcome page.
- Lets check that the Persistent Volume is correctly mounted inside the container.
- Open the Pod page and go to the **Terminal** tab.
- Type in command **df -h** and you should see a volume sized about 10Gib mounted in /var/www/html
<img src="https://raw.githubusercontent.com/jaanae/devops-workshop/master/pod-cli-df.png" width="60%" height="60%">

- Also you can type in **vi /var/www/html/index.html**. This command will create a new index.html file.
- Click **i** to start typing with the vi text editor. If you know how, you can create a simple html web page here. Otherwise you can just type in something and the webpage will show what you have typed. 
- Hit **ESC** and type **:wq!** and hit enter. this will save and close the **vi** text editor. Now if you click the Route link again, you should see your new "webpage"

## THE FINAL WEEK IS NOW DONE, CONGRATULATIONS!
Now if you have time and energy, you can create a new application of your choice in the OpenShift cluster. Be aware though that the cluster will be deleted in a few weeks and we will be monitoring that created applications do not contain anything illegal or otherwise not "good" things like bitcoin miners etc. Happy creating :)
- we will inform in the Slack channel when the cluster will be deleted!

More detailed reading about OpenShift can be found in the official RedHat OpenShift Documentation: https://docs.openshift.com/container-platform/4.6/welcome/index.html











