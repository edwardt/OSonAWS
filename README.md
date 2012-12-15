OSonAWS
=======

OS templates on AWS

All json files will be merged into one big template which creates swift cluster. It's zone and account free.


TODO 

- Use VPC instead of Public IPs

-- Keystone template
Launch the template in AWS (need to correct AMIs in mapping to Ubuntu12.04.1 LTS)
To verify keystone :
# TEST (replace OS_PASSWORD by swift user password parameter
export OS_USERNAME=swift
export OS_PASSWORD=icXyuCaywR
export OS_TENANT_NAME=service
export OS_AUTH_URL=http://127.0.0.1:35357/v2.0
keystone endpoint-get --service object-store

-- Swift node template
Carefull, launchconfig with 3 EC2 instances.