# EC2CloudFormationTemplate
A cloudformation template to provision a web server in a public subnet of a VPC in AWS.

A VPC is a logically isolated network in a cloud. A subnet is a logical division of the VPC, as per the resource network requirements. They can be either Public or Private.

A public subnet consists of a route from your EC2 resource to the Internet Gateway. A private subnet consists of routes between all resources in the VPC but not to the Public Subnets. Multiple subnets can be created within a VPC based on the size of the VPC. 

In this project, we create an EC2 Amazon Linux 2 resource within a public subnet with an Elastic IP Address. An Elastic IP address assigns a static public IP address to your EC2 instance, which is retained even when the instance is rebooted. Apart from this, common resources like route tables and security groups have been created. You are free to modify the resources/rules to suit your requirements. 

The parameters to the template are OwnerContact, WorkStationIP(IP which would SSH to EC2), KeyName and InstanceTypeParameters(t1.micro, t2.small, m1.large etc).

The reference documentation can be found here: https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/cfn-ug.pdf
