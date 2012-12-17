This project is experimental.

OSonAWS is a set of template to quickly deploy an OpenStack cloud on Amazon Web Services.

If you want to deploy OpenStack on a single machine for development, you should see http://devstack.org.

# Goals

* To quickely build OpenStack environment with many servers, network and storage (like a swift cluster).

BE CAREFUL : by default 5 EC2 instances (Keystone, SwiftProxy, 3x SwiftNodes) are launch with 3x1 Go EBS storage.

# Start a QA Cloud

Load swift template in AWS Cloudformation. 

See the output and launch the command from a system with swift client installed.
