==========================================================
  OpenStack over Amazon Web Services
==========================================================

:Version: 0.1 
:Keywords: Multi node OpenStack, Folsom, Quantum, Nova, Keystone, Glance, Horizon, Cinder, OpenVSwitch, Qemu, Ubuntu Server 12.04 (64 bits).
:Launchpad: https://launchpad.net/osonaws
:Status: Development

Table of Contents
=================

::

  1. What is it?
  2. How to launch my stack ?
  2. Pricing (AWS fees)
  3. Development rules
  4. Credits

  
Authors
==========

Copyright (C) Pierre FREUND <pierre.freund@osones.com>

1. What is it?
==============

OSonAWS is a set of template to quickly deploy an OpenStack cloud on Amazon Web Services.

OSonAWS launch a stack with minimum 7 servers according to the fallowing schema. You can choose when you launch the stack the amount of storage and the number/power of Nova nodes.
You can also add a swift cluster with the number of nodes and storage you want.

1. How to launch my stack ?
==============

For launching the template in CloudFormation, please refer to INSTALL.rst [https://github.com/pfreund/OSonAWS/blob/master/doc/INSTALL.rst]

How to access VMs / GUI ?
====================
.. image:: https://raw.github.com/pfreund/OSonAWS/master/doc/readme_images/access.png

How does the VPC is configured ?
====================
.. image:: https://raw.github.com/pfreund/OSonAWS/master/doc/readme_images/vpc.png

2. Default configuration and pricing (USA East)
====================

Default configuration :
* 4 EC2 Compute Units
* 15 Go RAM
* 100 Go DISK

:Size:Number:Unit price:Total price
:t1.micro:5:0,020:0,1
:m1.large:3:0,26:0,78

* Total : 0,88$ per hour.

3. Development rules
====================

* Only 1 file for launching a stack. No external files used in the template (wget, file section, etc)
* No specific AMI. Only use Ubuntu 12.04.1 LTS AMI.

4. Credits
=================

This work has been based on:

* Emilien Macchi's Folsom guide [https://github.com/EmilienM/openstack-folsom-guide]
* OpenStack Folsom Install Guide [https://github.com/mseknibilel/OpenStack-Folsom-Install-guide/blob/master/OpenStack_Folsom_Install_Guide_WebVersion.rst]
* OpenStack Documentation [http://docs.openstack.org/trunk/openstack-compute/install/apt/content/]
* OpenStack Quantum Install [http://docs.openstack.org/trunk/openstack-network/admin/content/ch_install.html]