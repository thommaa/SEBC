* List the cloud provider you are using (AWS, GCE, Azure, CloudCat, other)
  * AWS - eu-west-1 - Ireland center
  * running 5 instance of type: m3.xlarge
* List your instances by IP address and DNS name (don't use /etc/hosts for this)
  ```

  ```
* List the Linux release you are using
  Using the AMI ami-af6faad8: RHEL-6.5_HVM_GA-x86_64 (running ``yum update``)
  ```
[root@ip-172-31-23-52 ~]# cat /etc/redhat-release
Red Hat Enterprise Linux Server release 6.9 (Santiago)
  ```

* List the file system capacity for the first node
  ```
  [root@ip-172-31-23-52 ~]# lsblk && df -h
  NAME    MAJ:MIN RM SIZE RO TYPE MOUNTPOINT
  xvda    202:0    0  50G  0 disk
  └─xvda1 202:1    0  50G  0 part /
  Filesystem      Size  Used Avail Use% Mounted on
  /dev/xvda1       50G  2.5G   45G   6% /
  tmpfs           7.3G     0  7.3G   0% /dev/shm
  ```
  List the command and output for yum repolist enabled
```
[root@ip-172-31-23-52 ~]# yum repolist enabled
Loaded plugins: amazon-id, rhui-lb, search-disabled-repos, security
repo id                                          repo name                                                                      status
rhui-REGION-client-config-server-6               Red Hat Update Infrastructure 2.0 Client Configuration Server 6                     8
rhui-REGION-rhel-server-releases                 Red Hat Enterprise Linux Server 6 (RPMs)                                       19,617
rhui-REGION-rhel-server-rh-common                Red Hat Enterprise Linux Server 6 RH Common (RPMs)                                129
repolist: 19,754
```
