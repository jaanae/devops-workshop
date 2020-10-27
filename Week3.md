 # Viikko 3
 
 ## Managing storage in OpenShift
  

Last week we created a wordpress application that uses mysql as a database. The mysql server that was deployed in a container did not have storage in itself to store the data from the wordpress. For this reason a persistent volume was requested from openshift with a persistent volume claim. 

- OpenShift uses persistent volumes to manage storage. Persistent volumes or PVs enable all kinds of storage to be used with the benefit that the application or the developer does not need to know what or where the storage really is.

- OpenShift Administrators can create PVs that can be storage for example from Cloud, NFS server or VMware VMDK storage. Check more about PVs here: https://docs.openshift.com/container-platform/4.4/storage/understanding-persistent-storage.html

- Developers can request storage for their applications by creating a Persistent Volume Claim or PVC. The developers tells the PVC, how much storage the application needs and what type of storage it needs if the OpenShift cluster has multiple storage options. The PVC then automatically grabs and binds the most appropriate Persistent Volume for the application. 



OpenShift uses the Kubernetes persistent volume (PV) framework to allow cluster administrators to provision persistent storage for a cluster. Developers can use persistent volume claims (PVCs) to request PV resources without having specific knowledge of the underlying storage infrastructure. In this workshop, you work as a developer and you will be using dynamically provisioned persistent volumes. In some cases the persistent volumes are not provisioned dynamically but instead they are provisioned manually by a cluster administrator. With manual provisioning, the developer creates a persistent volume claim and then the administrator will create and assing a persistent volume to bind to the claim. 

reatin reclaim policy allows manual reclamation of the resource for those volume plug-ins that support i

delete reclaim policy deletes both the PersistentVolume object from OpenShift Container Platform and the associated storage asset in external infrastructure, such as AWS EBS or VMware vSphere.



  <img src="https://raw.githubusercontent.com/jaanae/devops-workshop/master/account-information.png" width="60%" height="60%">
   - Luo volume 
   - Luo volumeClaim
   - MySQL (https://kubernetes.io/docs/tutorials/stateful-application/mysql-wordpress-persistent-volume/)
   
 
