# Detailed Steps to Follow to Get Connected to the BrainHack Cloud

This is an intro to getting connected to the BrainHack Cloud. There is already a lot of useful information in their [website documentation](http://brainhack.org/brainhack_cloud/docs/). However, this gives a step by step detailed guide to avoid some problems. All these added precisions come from questions that sparked when following the tutorials.


### **Step 1. Obtaining your oracle account username and password** 
-  Follow [this link](http://brainhack.org/brainhack_cloud/docs/request/) to request resources by adding a GitHub issue and then activating your account on the oracle cloud infrastructure

### **Step 2. Configuring your HPC cluster via the Oracle platform**
- Now, follow [this link](http://brainhack.org/brainhack_cloud/tutorials/hpc/) to create your first job on the oracle platform, the bullet points below will give precisions on some aspects that aren't specified precisely on their tutorial:
- When downloading the Terraform zip, choose the oci-hpc-clusternetwork-2.8.0.5.zip and NOT oci-hpc-2.8.0.5.zip
- When configuring your HPC cluster, there comes a time to create an SSH key for connection purposes. Follow their [provided link](http://brainhack.org/brainhack_cloud/tutorials/vm/#create-a-public-key) and scroll to the *Create a public key* section. It is **important** to generate your public key not on the cloud shell as shown but rather on the computer you want to access the cloud from. This will be better for copying the data you need to analyze later! However, if by mistake you created your ssh key only on the cloud shell and associated that one when applying your first job (as shown in their tutorial), then here is what can be done:
    - Create a cluster user using the “cluster user add” command as described in the tutorial. This user can then connect to the cluster with lower security settings (e.g. by using password only!)
    
    OR

    - Download the SSH keys of the cloudshell and use the opc (=admin) account from your own computer (linux or WSL terminal)
    
*Note. These two options have kindly been provided by Steffen Bollmann and adapted from an email exchange.*

### **Step 3. Connecting to the cloud from your own computer via SSH**
Now that everything is configured correctly, it is now time to connect remotely via SSH to the cloud.
*Note. These steps were done on a WSL terminal*

The two options for connecting are:
- Creating a cluster user to work in as explained above is usually a better practice than working directly on the opc (admin account) because it requires the lowest privileges. It will indeed just ask for the password you have set up each time you connect. For connecting type this command in the terminal:

    ```console
    user@LAPTOP-abcdefgh:~$ ssh cluster_user_name@bastion-ip
    ```

    And it will show:
    ```console
    cluster_user_name@bastion-ip's password:  
    Creating directory '/home/cluster_user_name'. 
    [cluster_user_name@ace-swift-bastion ~]$                      
    ```

- Connecting directly to the admin account via this command:

    ```console
    user@LAPTOP-abcdefgh:~$ ssh -i ~/.ssh/oracle_private_key_file_name opc@bastion-ip
    ```
    Here, ssh -i links to the input ssh key which needs to be read in order to successfully connect to the cloud. If the connection worked it will show:
    ```console
    Last login: Thu Jul 25 15:34:25 2022 from 22.456.34.12
    [opc@ace-swift-bastion ~]$

    ```
Finally, type in exit in the command line to logout.

Congrats :tada: :sparkler:! You have now successfully connected to an HPC cluster on the BrainHack Cloud :brain:! Happy analyzing :computer: :chart_with_upwards_trend:!
