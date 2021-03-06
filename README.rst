!! WARNING, openstack.template does not work yet, due to a network problem. You can launch the stack, connect to the GUI, but openstack instances does not start properly !!


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
  3. Parameters
  3. What will be installed ?
  4. Pricing (AWS fees)
  5. Development rules
  6. Credits

  
Authors
==========

Copyright (C) Pierre FREUND <pierre.freund@osones.com>

1. What is it?
==============

OSonAWS is a set of template to quickly deploy an OpenStack cloud on Amazon Web Services.

OSonAWS launch a stack with minimum 7 servers according to the fallowing schema. You can choose when you launch the stack the amount of storage and the number/power of Nova nodes.
You can also add a swift cluster with the number of nodes and storage you want.

2. How to launch my stack ?
==============

First, you should have an AWS account with access to CloudFormation and a valid keypair. If you don't, please fallow AWS Getting Started webpage :

   http://docs.amazonwebservices.com/AWSEC2/latest/UserGuide/EC2_GetStarted.html

* Open this URL in a browser and save the file (File > Save as) :

   https://raw.github.com/pfreund/OSonAWS/master/openstack.template

* Open your AWS console and go to CloudFormation tab. Click "create new stack",
* Give your stack a name and load the template you downloaded on step 1. Then press continue,
* Find in the parameter list "Keyname" and give the name of your EC2 keypair. Check in the IAM ressource validation box,
* Press continue until the end of the wizard.
* Wait around 30 minutes and connect to OpenStack GUI via URL given in output tab of your stack.
* Click in "outputs" tab and click on the URL : "Horizon URL".
* Connect on the dashboard with admin/password, or demo/password. Note that you can change demo login and passwords in the template parameters.

!! Don't forget to SUPRESS your stack after use !!

3. Parameters
==============

What do I need to change ?
====================
* Keyname : Put the name of your existing keypair

What should I change ?
====================
* CinderVolumeSize : If you need more Cinder space.
* Passwords : mysql root, mysql user, service tenant, keystone admin token, Rabbit.
* Horizon credentials : Demo/admin login and passwords.
* Project Name : Name of the project in GUI.
* SSH private/public key : used to connect between nodes via ssh.

What can I change if I know what I'm doing ?
====================
* InstanceType : If you want larger OpenStack hosts (keystone, cinder, glance, nova).
* ComputeInstanceType : Nova Compute size.
* QuantumInstanceType : Quantum server size, please note that Quantum MUST have 3 ENI.

4. What will be installed ?
==============

Services / hosts
====================
.. image:: https://raw.github.com/pfreund/OSonAWS/master/doc/readme_images/services.png

Access
====================
.. image:: https://raw.github.com/pfreund/OSonAWS/master/doc/readme_images/access.png

VPC Configuration
====================
.. image:: https://raw.github.com/pfreund/OSonAWS/master/doc/readme_images/vpc.png


5. Default configuration and pricing (USA East)
====================

Openstack ressources available by default :

* 4 EC2 Compute Units
* 15 Go RAM
* 100 Go DISK

AWS ressources price :

===== ========= ====== ============= ===========
Type  Size      Number Price         Total
EC2   t1.micro  5      0,020/hour    0,1
EC2   m1.large  3      0,26/hour     0,78
EBS   standard  100 Go 0,10/Go/month 0,013
===== ========= ====== ============= ===========

Total : around 1$/hour with traffic.

6. Development rules
====================

* Only 1 file for launching a stack. No external files used in the template (wget, file section, etc)
* No specific AMI. Only use Ubuntu 12.04.1 LTS AMI.

7. Credits
=================

These guides has been very helpful.

* Emilien Macchi's Folsom guide [https://github.com/EmilienM/openstack-folsom-guide]
* OpenStack Folsom Install Guide [https://github.com/mseknibilel/OpenStack-Folsom-Install-guide/blob/master/OpenStack_Folsom_Install_Guide_WebVersion.rst]
* OpenStack Documentation [http://docs.openstack.org/trunk/openstack-compute/install/apt/content/]
* OpenStack Quantum Install [http://docs.openstack.org/trunk/openstack-network/admin/content/ch_install.html]