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
- Change the names and namespace names in the example with your pod and namespace names.
- Click **Create** and check that the pod is in running state. The pod initialization can take up to few minutes.
<img src="https://raw.githubusercontent.com/jaanae/devops-workshop/master/pod-running.png" width="60%" height="60%">


# 3. Creating a Service

-
-

# 4. creating a Route

-
-



