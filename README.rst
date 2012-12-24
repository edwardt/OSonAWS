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
  1. Requirements
  2. Launch a stack
  3. Pricing (AWS fees)

0. What is it?
==============

OSonAWS is a set of template to quickly deploy an OpenStack cloud on Amazon Web Services.

Version 0.1

Status: Development 

1. Requirments
====================

To use OSonAWS, you need to have a valid account on AWS and a keypair on EC2 service. If you don't, please fallow AWS Getting Started webpage :
http://docs.amazonwebservices.com/AWSEC2/latest/UserGuide/EC2_GetStarted.html

2. How to use?
====================

2.1. Download openstack.template on GitHub.
-----------------

2.2 Open your AWS console and go to CloudFormation tab. Click "create new stack".
-----------------

.. image:: http://s3-ap-southeast-1.amazonaws.com/osonaws/howto/createstack.png

2.3 Give your stack a name and load the template you downloaded on step 1. Then press continue.
-----------------

.. image:: http://s3-ap-southeast-1.amazonaws.com/osonaws/howto/nameandtemplate.png

2.4 Find in the parameter list "Keyname" and give a the name of one of your EC2 keys. Check in the IAM ressource validation. Then press continue until the end.
-----------------

.. image:: http://s3-ap-southeast-1.amazonaws.com/osonaws/howto/keynameIAM.png

2.5 Wait around 30 minutes and connect to OpenStack GUI via URL given in output tab of your stack.
-----------------

.. image:: http://s3-ap-southeast-1.amazonaws.com/osonaws/howto/createinprogress.png

.. image:: http://s3-ap-southeast-1.amazonaws.com/osonaws/howto/createcomplete.png

2.6 Click in "outputs" tab and click on the URL : "Horizon URL".
-----------------

.. image:: http://s3-ap-southeast-1.amazonaws.com/osonaws/howto/output.png

2.7 Connect on the dashboard with admin/password, or demo/password. Note that you can change demo login and passwords in the template parameters.
-----------------

.. image:: http://s3-ap-southeast-1.amazonaws.com/osonaws/howto/login.png