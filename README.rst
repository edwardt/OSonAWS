==========================================================
  OpenStack over Amazon Web Services
==========================================================

:Version: 0.1 
:Keywords: Multi node OpenStack, Folsom, Quantum, Nova, Keystone, Glance, Horizon, Cinder, OpenVSwitch, KVM, Ubuntu Server 12.04 (64 bits).
:Launchpad: https://launchpad.net/osonaws
:Status: Development

Table of Contents
=================

::

  1. What is it?
  2. Pricing (AWS fees)
  3. Development rules
  4. Credits

  
Authors
==========

Copyright (C) Pierre FREUND <pierre.freund@gmail.com>

1. What is it?
==============

OSonAWS is a set of template to quickly deploy an OpenStack cloud on Amazon Web Services.

OSonAWS launch a stack with minimum 7 servers according to the fallowing schema. You can choose when you launch the stack the amount of storage and the number/power of Nova nodes.
You can also add a swift cluster with the number of nodes and storage you want.

.. image:: http://s3-ap-southeast-1.amazonaws.com/osonaws/howto/schema.png

2. Pricing
====================

Default configuration :
12 cores / 22,5 Go RAM / 100 Go DISK

5 small instances : 0,065$ * 5 = 0,325 $
3 large instances (compute) 0,260$ * 3 = 0,78 $

Total : 1$ / hour

3. Development rules
====================

* Only 1 file for launching a stack. No external files used in the template (wget, file section, etc)
* No specific AMI. Only use Ubuntu 12.04.1 LTS AMI.

4. Credits
=================

This work has been based on:

* Emilien Macchi's Folsom guide [https://github.com/EmilienM/openstack-folsom-guide]
* OpenStack Documentation [http://docs.openstack.org/trunk/openstack-compute/install/apt/content/]
* OpenStack Quantum Install [http://docs.openstack.org/trunk/openstack-network/admin/content/ch_install.html]