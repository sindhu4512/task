---
layout: default
title:  ""
permalink: /CLI/
---

## User Story 1.1.2: Command Line Guided Installation 

Use this procedure to perform basic setup without any changes or physical installation options.

**Note:** You can use [Script Guided Installation](https://doc.owncloud.com/server/admin_manual/installation/manual_installation/script_guided_install.html) to improvise the setup. 


### Procedure to install using command line:

1. Extract the archive contents and run the unpacking command for the tar archive:

		$ tar -xjf owncloud-complete-yyyymmdd.tar.bz2
	
	The tar file unpacks to a single owncloud directory.
	
2. Copy the ownCloud directory to its final destination using the following command: 

		$ cp -r owncloud /var/www
		
**Note:** The $/var/www is the root directory location. Replace if your files are stored in different directory. 

3. Finalize the installation: 
For example, if the source is unpaked to /var/www/owncloud/

		$ cd /var/www/owncloud/
		$ sudo -u www-data php occ maintenance:install \
	 	  --database "mysql" --database-name "owncloud" \
	  	 --database-user "root" --database-pass "password" \
 	  	 --admin-user "admin" --admin-pass "password"
	   
**Note:** For detailed OCC usage, see [OCC Command Reference](https://doc.owncloud.com/server/admin_manual/configuration/server/occ_command.html). 

The ownCloud is successfully downloaded and installed. 

**Note:** ownCloud recommends to perform some post installation tasks to configure background jobs or improve performance by caching. For more information, see [Post Installation](https://doc.owncloud.com/server/admin_manual/installation/manual_installation/manual_installation.html#post-installation-configuration)
