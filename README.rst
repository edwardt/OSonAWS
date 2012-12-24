==========================================================
  OpenStack over Amazon Web Services
==========================================================

:Version: 0.1 Alpha
:Keywords: Multi node OpenStack, Folsom, Quantum, Nova, Keystone, Glance, Horizon, Cinder, OpenVSwitch, KVM, Ubuntu Server 12.10 (64 bits).
:Authors: Pierre FREUND <pierre.freund@gmail.com>

Table of Contents
=================

::

  0. What is it?
  1. Launch a stack?

0. What is it?
==============

OSonAWS is a set of template to quickly deploy an OpenStack cloud on Amazon Web Services.

Version 0.1

Status: Development 


1. How to use?
====================

**Step 1:** Download openstack.template on GitHub.



**Step 2:** Open your AWS console and go to CloudFormation tab.



**Step 3:** Launch a new stack with openstack.template file.




**Step 4:** Wait around 30 minutes and connect to OpenStack GUI via URL given in output tab of your stack.

.. image:: http://s3-ap-southeast-1.amazonaws.com/osonaws/howto/createinprogress.png
.. image:: http://s3-ap-southeast-1.amazonaws.com/osonaws/howto/createcomplete.png

