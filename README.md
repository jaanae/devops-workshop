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
 
 7. On your cloud dashboard, click your account name on the right top corner and choose "IBM Forum Helsinki".
 <img src="https://raw.githubusercontent.com/jaanae/devops-workshop/master/cloud-dashboard.png" width="60%" height="60%">
 
 8. 
 <img src="https://raw.githubusercontent.com/jaanae/devops-workshop/master/cloud_burger_menu.png" width="60%" height="60%">

 4. Click kubernetes.   
 <img src="https://raw.githubusercontent.com/jaanae/devops-workshop/master/cloud_kubernetes.png" width="60%" height="60%">

 5. Click create cluster.   
 <img src="https://raw.githubusercontent.com/jaanae/devops-workshop/master/cloud_create_cluster.png" width="60%" height="60%">

 6. Configure your cluster. Select free plan, default resource group and give your cluster a name. Then click "Create" on the bottom right corner.
 <img src="https://raw.githubusercontent.com/jaanae/devops-workshop/master/cloud_configure_cluster.png" width="60%" height="60%">

7. When your cluster has been created you can go to the kubernetes overview page.
<img src="https://raw.githubusercontent.com/jaanae/devops-workshop/master/cloud_cluster_created.png" width="60%" height="60%">

8. >FROM HERE ON these prolly wont go to the final workshop depending if we decide to proceed with the command line route or the GUI route... 

9. Following is to test that kubernetes functions properly.
Click somewhere (need to check what button and where as I dont seem to have a screenshot) to open cluster and click nodes and then click your node.
>image of that here!

10. Find your clusters public IP address and mark it down. We'll need that later.
<img src="https://raw.githubusercontent.com/jaanae/devops-workshop/master/cloud_external_ip.png" width="60%" height="60%">

11.Back on the overview page. Open the kubernetes web terminal by clicking Actions and then click web terminal on the upper right corner of the overview page.
<img src="https://raw.githubusercontent.com/jaanae/devops-workshop/master/cloud_open_webterminal.png" width="60%" height="60%">

12. A web terminal opens.
<img src="https://raw.githubusercontent.com/jaanae/devops-workshop/master/cloud_terminal.png" width="60%" height="60%">

13. On the terminal type the following commands.
>commands from the picture here
<img src="https://raw.githubusercontent.com/jaanae/devops-workshop/master/cloud_terminal_commands.png" width="60%" height="60%">

14. Go to your clusters public IP address with your browser. If you see nginx welcome page, your kubernetes cluster works as intended! yay!
>picture of the nginx welcome page here.
