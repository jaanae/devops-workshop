 # Viikko 0
 - Tunnareiden luonti (Eelia)
 
 # Viikko 1
  - Kirjautu OC:lle UI (Jaana)
  - Asentaa command line toolin OC:lle (Jaana)
  - Kirjautua Oc:llä clusteriin (Terminal) --> (Jaana)
  - Luo projektin OC:lle (*-omanimi) (Eelia)
  - Lataa snake imagen Developer näkymästä (Eelia)

 # Viikko 2
  Kaikki terminaalin kautta:
   - Luo uuden projektin 
   - Lisää ImageSteam
   - Lisää BuildConfig
   - Kirjoittaa deployment-config.yml 
   - Luodaan service
   - Luodaan route
   
 # Viikko 3
  Jatkuu sama projekti  
   - Luo volume 
   - Luo volumeClaim
   - 
  
 # Viikko 4
  -
 
 
 
 
 
 1. Create an IBM cloud account!
 >tähän kuva tunnarin luomisesta
 
 2. Login to IBM Cloud.
 <img src="https://raw.githubusercontent.com/jaanae/devops-workshop/master/cloud_login.png" width="60%" height="60%">
 
 3. Open burger menu on the top left corner.
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
