---
layout: default
title:  ""
permalink: /Downloading/
---

## Downloading owncloud

#### Prerequisites: 
Change the directory location to save the file temporarily. The format of the folder name should be _owncloud-complete-yyyymmdd.archive_type_. 

1. Download the required package from [ownCloud Download Page](https://owncloud.com/download-server/).
	There are two download options available:
	
	-.tar.bz2 
	
	-.zip
	
2. Run the following command:

		$ wget https://download.owncloud.org/community/owncloud-complete-yyyymmdd.tar.bz2

3. Download the corresponding checksum file using the following command: 

		$ wget https://download.owncloud.org/community/owncloud-complete-yyyymmdd.tar.bz2.md5
								or						
		$ wget https://download.owncloud.org/community/owncloud-complete-yyyymmdd.tar.bz2.sha256

4. Verify the _MD5_ or _SHA256_ sum using the following command: 

		$ sudo md5sum -c owncloud-complete-yyyymmdd.tar.bz2.md5 < owncloud-complete-yyyymmdd.tar.bz2
								or
		$ sudo sha256sum -c owncloud-complete-yyyymmdd.tar.bz2.sha256 < owncloud-complete-yyyymmdd.tar.bz2
	
5. Verify the PGP signature using the following command:

		$ wget https://download.owncloud.org/community/owncloud-complete-yyyymmdd.tar.bz2.asc
								or 
		$ gpg --verify owncloud-complete-yyyymmdd.tar.bz2.asc owncloud-complete-yyyymmdd.tar.bz2
