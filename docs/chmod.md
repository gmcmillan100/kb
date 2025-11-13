---
layout: page
title: chmod
permalink: /chmod/
resource: true
---

chmod = Change File Modes

# Owner, group, world

	644 = -rw-r--r-- = owner can read and write, group can read, rest of world can read

	777 = -rwxrwxrwx = all can read, write, and execute

```
$ chmod 644 notes
$ ls -l notes
total 17800
drw-r--r--    4 gmcmilla gmcmilla    16384 Jul 19 15:27 notes
```

# Values

```
Value	Permission				Directory Listing
-----------------------------------------------------------------
 0	No read, no write, no execute		---
 1	No read, no write, execute		--x
 2	No read, write, no execute		-w-
 3	No read, write, execute			-wx
 4	Read, no write, no execute		r--
 5	Read, no write, execute			r-x
 6	Read, write, no execute			rw-
 7	Read, write, execute			rwx
 ```

## chown

To change ownership of "getall.php" to "gmcmilla":

 ```
sudo chown gmcmilla getall.php
iwww-test.corp:gmcmilla[585] /export/apps/apache2/iwww-test/htdocs $ ls -al getall.php
-rwxr-xr-x   1 gmcmilla webservd     668 Dec  7 01:04 getall.php*
 ```

## chgrp

To change the group from "gmcmilla" to "webservd":

 ```
esv4-cms01.corp:gmcmilla[563] /export/apps/apache2/htdocs/stats $ ls -al getall.php
-rwxr-xr-x   1 gmcmilla gmcmilla     668 Jan 10 16:47 getall.php*
esv4-cms01.corp:gmcmilla[564] /export/apps/apache2/htdocs/stats $ sudo chgrp webservd getall.php
Password:
esv4-cms01.corp:gmcmilla[565] /export/apps/apache2/htdocs/stats $ ls -al getall.php
-rwxr-xr-x   1 gmcmilla webservd     668 Jan 10 16:47 getall.php*
 ```