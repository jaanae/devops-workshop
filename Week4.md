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
   + **Hint!** [Check how to create the PVC here](/httpd-pvc.png)

# 2. Deploying the httpd Pod

-
-

# 3. Creating a Service

-
-

# 4. creating a Route

-
-



