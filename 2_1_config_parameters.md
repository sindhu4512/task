---
layout: default
title:  ""
permalink: /Config/
---

## Config.php Parameters    

ownCloud uses **config/config.php file** control server operations.   

>**Note**: To do the changes on Debian/Ubuntu Linux operating systems, you need to edit these files:

-	/etc/apache2/sites-enabled/owncloud.conf  
-	/var/www/owncloud/config/config.php  

### Use the following commands to edit the Default Parameters, once **config.php** file has been configured by the ownCloud serve. 
  

 *    'trusted_domains' =>
		array (
		'demo.example.org',
        'otherdomain.example.org',
      )

This gives a list of trusted domains that users can log into. 

**Note** The admin is not supposed to remove this, as it performs necessary security checks.


	*  'dbhost' => 'x.x.x.x:8080'
	
	where x.x.x.x is server’s IP address.
	
This defines the host server name, for example **localhost**, **hostname**, **hostname.example.com**, or the **IP address**. To specify a port use **hostname:####**  

    
   

 

### Default config.php Example- This is how your config.php will look like after installing ownCloud using MySQL database. **config/config.sample.php** lists all the configurable parameters within ownCloud.

    <?php
    $CONFIG = array (
      'instanceid' => 'oc8c0fd71e03',
      'passwordsalt' => '515a13302a6b3950a9d0fdb970191a',
      'trusted_domains' =>
      array (
        0 => 'localhost',
        1 => 'studio',
        2 => '192.168.10.155'
      ),
      'datadirectory' => '/var/www/owncloud/data',
      'dbtype' => 'mysql',
       'version' => '7.0.2.1',
      'dbname' => 'owncloud',
      'dbhost' => 'localhost',
      'dbtableprefix' => 'oc_',
      'dbuser' => 'oc_carla',
      'dbpassword' => '67336bcdf7630dd80b2b81a413d07',
      'installed' => true,
    );  
    
Once the changes are done and all the files are saved, restart the Apache server. You can now access ownCloud from either, <https://example.com/> or <https://localhost/>.  