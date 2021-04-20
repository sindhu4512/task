---
layout: default
title:  ""
permalink: /Adding/
---


## User Story 3: Adding User Accounts to ownCloud Server  

User information consists of user profile and login details. The administrator can create new user accounts with the following properties:
* **Username(Login Name):** unique ID of the ownCloud user. This name cannot be changed.
* **Full Name:** display name of the user on the ownCloud user interface. This name can be changed by admin and users. 
* **E-mail:**  new e-mail address for user set by admin. 
* **Password:** password for the user account which is set by admin. The user can change the password after first time login. 
* **Groups:** each user is assigned a group depending on the membership. 
* **Quota:** maximum disk space assigned to each user.  
  
  
### Procedure to add a new user account: 

1. Log in to the _ownCloud server_ portal as an administrator.
   The _User administration_ page appears. 
   
    
2. Click **admin** on the top right corner of the page. 

   A drop-down menu appears. 
   
    ![3 1](https://doc.owncloud.com/server/10.7/admin_manual/_images/configuration/user/users-page-new-user.png)  
   
   
 
3. From the drop-down menu, select **Users**.

   The _User Information_ page with all the exsisting user information appears. 
   
    ![3 2](https://doc.owncloud.com/server/10.7/admin_manual/_images/configuration/user/users-page.png)  

4. In the **Username** field, type the username (login name). 

	**Note:** 

	* Login names contains letters (a-z, A-Z), numbers (0-9), dashes (-), underscores (_), periods (.), and at signs (@).

	* ownCloud usernames cannot be changed, once set. 
	
5. In the **Password** field, type the password. 

	**Note:** This initial password should be shared with the individual user. 

6. From the drop-down list, select and assign a group based on the user membership. For more information on the groups,
 [User Groups](https://sindhu4512.github.io/task/Creating/). 
 
 **Note:** This step is optional. 

7. Click **Create**.
   The new user account is created.   

**Note**: To ensure the new entry is visble, refresh the page by pressing _Ctrl-R_.    

  

          
