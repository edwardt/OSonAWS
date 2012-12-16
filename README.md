OSonAWS -- OpenStack on Amazon Web Services
===========================================

1 template, 1 cloud.

This template creates an OpenStack cloud on AWS.

First step, create a swift cluster with Swift. Done 90%.

Second step, create nova/cinder/quantum. Done 0%

==========
How to use
==========

Just go to cloud formation and launch the template.
It's account free, it's zone free.

Careful, by default 5 EC2 instances (Keystone, SwiftProxy, 3x SwiftNodes) are launch with 3x1 Go EBS storage.