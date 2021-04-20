---
layout: default
title:  ""
permalink: /Port/
---

## Changing the Proxy Configurations  

The automatic hostname, protocol or webroot detection of ownCloud can fail in certain reverse proxy situations. This configuration allows the automatic detection to be manually overridden. You can find the detailed explanation in the [Overwrite Parameters]( https://doc.owncloud.org/server/10.0/admin_manual/configuration/server/reverse_proxy_configuration.html#overwrite-parameters) section.  

    'overwritehost' => '',
	
This option allows you to manually override the automatic detection; for example **www.example.com**, or specify the port **www.example.com:8080**.

    'overwriteprotocol' => '',
	
When generating URLs, ownCloud attempts to detect whether the server is accessed via **https** or **http**. However, if ownCloud is behind a proxy and the proxy handles the **https** calls, ownCloud would not know that **ssl** is in use, which would result in incorrect URLs being generated.  

    'overwritewebroot' => '',
	
ownCloud attempts to detect the webroot for generating URLs automatically.
For example, if **www.example.com/owncloud** is the URL pointing to the ownCloud instance, the webroot is **/owncloud**. When proxies are in use, it may be difficult for ownCloud to detect this parameter, resulting in invalid URLs.

    'overwritecondaddr' => '',
	
This option allows you to define a manual override condition as a regular expression for the remote IP address. For example, defining a range of IP addresses starting with **10.0.0.** and ending with 1 to 3: **^10\.0\.0\.[1-3]$**

    'overwrite.cli.url' => '',
	
Use this configuration parameter to specify the base URL for any URLs which are generated within ownCloud using any kind of command line tools (cron or occ). The value should contain the full base URL: **https://www.example.com/owncloud**