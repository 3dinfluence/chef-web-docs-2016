.. The contents of this file may be included in multiple topics.
.. This file should not be changed in a way that hinders its ability to appear in multiple documentation sets.

Before installing the |chef server| software, perform the following steps:

#. Use an |amazon vpc|. |amazon ec2_classic| is not supported.
#. Create appropriate security groups to contain the backend instances. The only requirement for the |chef server| is that |icmp| is permitted between the two backend instances; |keepalived| requires it for communication and heartbeat.
#. Launch two servers, one for the primary backend |chef server| and the other for the secondary backend |chef server|. Use the same |amazon ami| so that both backend servers have identical platform and versions. The servers must be in the same |amazon zones|.
#. Create an |amazon ebs| volume to store the |chef server|'s data. It is recommended that you use an |amazon ebs_volume_provisioned| volume type, with the maximum IOPS ratio for the size of volume.
#. Decide on what IP address the backend virtual IP (VIP) will be. It must reside in the same network segment as the backend machines. It will be specified in the |chef server rb| file; during installation, the high-availability plugin will automatically assign the VIP to the |amazon eni| for the primary instance.
#. Create an |amazon iam| user with at least the permissions documented in the reference section. Record this user's access and secret keys; these will be used in the |chef server rb| configuration file.