# nfsminer-ng

A tool that uses standard Linux tools to enumerate NFS shares.

## Dependencies:
nfs-common

## Updates:
I added flags for setting the depth of folder recursions.  
I updated the file details collected to include:  Permissions, Last Modified Date, and File Size.

## Usage:
```
$ ./nfsminer-ng -h

NFS Miner
Created by Tim Jensen @eapolsniper
BSI CSIR - bsigroup.com

-t   --  Text file containing a list of IP's to scan. All exports on each host is scanned.
-s   --  Single host to scan. Scans all exports on host
-fd  --  Depth of folder recursions.  Default is 3.
-dt  --  Discovery Timeout. Useful for slow networks to skip over very slow hosts. Default 5 seconds.
-ft  --  File Scan Timeout. Sets maximum scan timeout for recursive filetype discovery, per host.  Default 10 minutes.
-df  --  Disables all file scanning, only discovers exports and lists top directory lists. This is very fast.
-du  --  Disables unmounting of all shares, allowing easy manual discovery/searching without having to remount the drives again.

----------------------
SLOW (I warned you) options
----------------------
-eg  --  Enable grep scans. Recursively searches all files for keywords
-gt  --  Grep scan timeout. Set maxiumum scan time for recursive grep scans, per host. Default 10 minutes.
```
