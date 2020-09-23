 # Viikko 0
 - Tunnareiden luonti (Eelia)
 
 # Viikko 1
  - Kirjautu OC:lle UI (Jaana)
  - Asentaa command line toolin OC:lle (Jaana)
  - Kirjautua Oc:llä clusteriin (Terminal) --> (Jaana)
  - Luo projektin OC:lle (*-omanimi) (Eelia)
  - Lataa snake imagen Developer näkymästä (Eelia)

 # Viikko 2
  * Kaikki terminaalin kautta:
  * Gitin kautta triggeri
   - Luo uuden projektin (Jaana)
   - Lisää ImageSteam (Jaana)
   - Lisää BuildConfig (Jaana)
   - Kirjoittaa deployment-config.yml (Eelia tai Jaana)
   - Luodaan service (Eelia tai Jaana)
   - Luodaan route (Eelia tai Jaana)
   
 # Viikko 3
  Jatkuu sama projekti
   - Luo volume 
   - Luo volumeClaim
   - MySQL (https://kubernetes.io/docs/tutorials/stateful-application/mysql-wordpress-persistent-volume/)
   
 # Viikko 4
  - Keratusviikko?
 
 
 
 
 
 1. To create an IBM cloud account, go to https://cloud.ibm.com/registration
 2. Type in your email and choose a password and click next.
 <img src="https://raw.githubusercontent.com/jaanae/devops-workshop/master/account-information.png" width="60%" height="60%">
 
 3. Check your email inbox for the verification code, type it to the field and click next.
 <img src="https://raw.githubusercontent.com/jaanae/devops-workshop/master/email-verification-code.png" width="60%" height="60%">
 
 4. Enter your personal information and click next.
 <img src="https://raw.githubusercontent.com/jaanae/devops-workshop/master/personal-information.png" width="60%" height="60%">
 
 5. Verify your information and click create account.
 <img src="https://raw.githubusercontent.com/jaanae/devops-workshop/master/create-account.png" width="60%" height="60%">
 
 6. Read and acknowledge the policies. Click proceed.
 <img src="https://raw.githubusercontent.com/jaanae/devops-workshop/master/acknowledgement.png" width="60%" height="60%">
 
 After account creation, you should land on the cloud dashboard page. on this page you can view and access all ibm cloud resources that you have created or that you are collaborating in. 
- At this point, wait until the workshop instructors have invited you to collaborate in the IBM Forum helsinki workspace in IBM Cloud. After the instructors have invited you, proceed to step 7.
 
 7. On your cloud dashboard, click your account name on the right top corner and choose "IBM Forum Helsinki".
 <img src="https://raw.githubusercontent.com/jaanae/devops-workshop/master/cloud-dashboard.png" width="60%" height="60%">
 
 8. When you have succesfully switched to the IBM Forum helsinki dashboard, you should see one cluster resource available to you on the left hand side of the dashboard. Click the "Clusters" link.
 <img src="https://raw.githubusercontent.com/jaanae/devops-workshop/master/open-clusters.png" width="60%" height="60%">

 9. On the resources page, click on the "ocp43-workshop"
 <img src="https://raw.githubusercontent.com/jaanae/devops-workshop/master/open-workshop.png" width="60%" height="60%">

 10. You should land on the ocp43-workshop dashboard page. Your account may not have sufficient credentials to view the cluster statuses on the right hand side nor the logging and monitoring components but dont worry, those are not needed for this workshop. 
 - Click on the blue "OpenShift Web Console" button on the right top corner of the dashbord. 
 - Opening the openshift web console trough this link is necessary only once. This is because clicking the link triggers a script that automatically creates a useraccount for you in openshift. Afterwards you can just bookmark the openshift web console address and open it straight up without going trough the ibm cloud. 
 <img src="https://raw.githubusercontent.com/jaanae/devops-workshop/master/ocp-workshop-ibm-cloud.png" width="60%" height="60%">

 11. Now you should land on the OpenShift Web Console Dashboard page. Dont worry if you are not able to see the cluster nodes, details, status, activity or events. The account that is automatically created for you has only "edit" rights for now and thus is not sufficient to view the cluster in more detail.
 <img src="https://raw.githubusercontent.com/jaanae/devops-workshop/master/ocp-dashboard.png" width="60%" height="60%">

# TÄHÄN VARMAAN NOI JAANAN KOMENTORIVISETIT SUN MUUT


12. At this point, wait until the instructors assing more privileges for your openshift user. The new role that you will get is called "self-provisioner". The privileges of "self-provisioner" are the same as your original "edit" role but with the added rights to create, edit and delete your own openshift projects.
- After you have been assigned as "self-provisioner", continue to the step 13.
- You can read more about the default roles and privileges here: https://docs.openshift.com/container-platform/4.3/authentication/using-rbac.html

13. From the OpenShift dashboard page, click open the home menu on the lefthand side of the page and click "projects". The projects page opens. Click "Create project" on the left top side of the page to create a new project.
 <img src="https://raw.githubusercontent.com/jaanae/devops-workshop/master/projects-page.png" width="60%" height="60%">
 
14. Create a new project and name it "projectname-myname". you can decide the project name yourself, a good example is "mimmitkoodaa-week1" and add your name after the project name.
- The project name must consist of lower case alphanumeric characters or '-', and must start and end with an alphanumeric character.
 <img src="https://raw.githubusercontent.com/jaanae/devops-workshop/master/create-project.png" width="60%" height="60%">
 
15. After the creation of the new project, you will land on the project dashboard page. This project will work as your own workspace for this workshop.
- Resources in projects are isolated from other projects by default.
 <img src="https://raw.githubusercontent.com/jaanae/devops-workshop/master/project-dashboard.png" width="60%" height="60%">
 
 # TÄNNE LISÄÄN VIELÄ PROJEKTIN LUOMISEN KOMENTORIVILTÄ JA MYÖS SEN POISTAMISEN
 
 
 
 
 
 
 
 
 
 
 
 
 
