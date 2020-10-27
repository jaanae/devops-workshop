 # Viikko 3
 
 ## Managing storage in OpenShift
  

Last week we created a wordpress application that uses mysql as a database. The mysql server that was deployed in a container did not have storage in itself to store the data from the wordpress. For this reason a persistent volume was requested from openshift with a persistent volume claim. 

- OpenShift uses persistent volumes to manage storage. Persistent volumes or PVs enable all kinds of storage to be used with the benefit that the application or the developer does not need to know what or where the storage really is.

- OpenShift Administrators can create PVs that can be storage for example from Cloud, NFS server or VMware VMDK storage. Check more about PVs here: https://docs.openshift.com/container-platform/4.4/storage/understanding-persistent-storage.html

- Developers can request storage for their applications by creating a PersistentVolumeClaim or PVC. The developers tells the PVC, how much storage the application needs and what type of storage it needs if the OpenShift cluster has multiple storage options. The PVC then automatically grabs and binds the most appropriate PersistentVolume for the application. 

# 1. Requesting storage / Creating a Persistent Volume Claim


- PVs can have three different reclaim policies. The reclaim policy of a PersistentVolume tells the cluster what to do with the volume after it is released. A volume’s reclaim policy is usually either **Retain** or **Delete**
    **a.** a Retain policy keeps the PV and its data alive even if the PVC is deleted. This enables the data to be reused and a new PVC to be bound to it.
    **b.** a Delete policy deletes the PV and its data when the PVC is deleted.

- First we create a PVC and see how it is bound to a PV. Choose a StorageClass with **Delete** reclaim policy.
<img src="https://raw.githubusercontent.com/jaanae/devops-workshop/master/create-pvc.png" width="60%" height="60%">


- When the PVC has been created, the OpenShift will begin to deploy a PersistentVolume to match the PVC.
- After the PV has been deployed, it will be automatically bound to the PVC and you will see the PVC status change to **Bound**. This means that the PVC now has storage attached to it and an application can start to use the PVC to store it's data. 
<img src="https://raw.githubusercontent.com/jaanae/devops-workshop/master/pvc-bound.png" width="60%" height="60%">

# 2. Releasing storage / Deleting a Persistent Volume Claim

- storage can be released by deleting the bound PVC. 
 
