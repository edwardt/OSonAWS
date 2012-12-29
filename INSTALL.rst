Table of Contents
=================

::

  1. Requirements
  2. Launch a stack

1. Requirements
====================

To use OSonAWS, you need to have a valid account on AWS and a keypair on EC2 service. If you don't, please fallow AWS Getting Started webpage :
http://docs.amazonwebservices.com/AWSEC2/latest/UserGuide/EC2_GetStarted.html

2. How to use?
====================

2.1. Download openstack.template on GitHub.
-----------------

Open this URL in a browser and save the file (File > Save as) :

https://raw.github.com/Capashen/OSonAWS/master/Openstack.template

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