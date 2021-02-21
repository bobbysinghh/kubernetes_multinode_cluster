# Ansible Role: ec2_create
=========

A simple Ansible role for create EC2 instance in AWS


Requirements
------------
Before starting you need the following packages on your ansible server
- epel-release
- python2-pip
- boto
- boto3


Role Variables
--------------


None of the variables below are required

| Variable                                     | Default                       | Comments                                                                                |
| :---                                         | :---                          | :---
| `aws_access_key`			                       |			                         | Inform AWS ACCESS KEY
|                                              |                               |
| `aws_secret_key`			                       |			                         | Inform AWS SECRET KEY
|                                              |                               |                                      
| `vpc_id_default `                            |                               | Inform VPC ID
|                                              |                               |
| `instance_type`         		                 |                               | Inform Instance Type examplo: t2.micro
|                                              |                               |
| `first_name`                                 |                               | Inform Instance Tags first name
|                                              |                               |
| `second_name`                                |                               | Inform Instance Tags second name examplo:   |                                              |                               |
| `environment_name`                           |                               | Inform Instance Tags environment             |                                              |                               | 
| `aws_region`				                         |			                         | Inform AWS Region exemplo Ohio: us-east-2
|						                                   |                               |
| `subnet1`				                             |                  			       | Inform default subnet exemplo default subnet Ohio 172.31.32.0/20: subnet-040acd48
|                                              |                               |
| `subnet2`				                             |   			                       | Inform default subnet exemplo default subnet Ohio 172.31.16.0/20: subnet-e5d14e9f
|                                              |                               |
| `subnet3`				                             |			                         | Inform default subnet exemplo default subnet Ohio 172.31.0.0/20: subnet-f78aac9f
|                                              |                               |
| `aws_image`				                           |			                         | Inform Image examplo Red Har 8: ami-05220ffa0e7fce3d1
|                                              |                               |
| `keypair_name`			                         |                   			       | Inform name for your key pair
|                                              |                               |
| `path`				                               |			                         | Where are you going to save the the key pair
|                                              |                               |
| `sg_group_name`			                         |                  			       | Inform Security Group name
|                                              |                               |
| `ssh_port`				                           |                  			       | Inform Port SSH default is 22
|                                              |                               |
| `cidr_ip_inbound`			                       |                  			       | Inform the IP allowed for ssh access examplo anywhere: 0.0.0.0/0
|                                              |                               |
| `cidr_ip_outbound`			                     |                  			       | Allow server access to the Internet
|                                              |                               | 
| `outbound_name`			                         |	                  		       | Inform OutBound name
|                                              |                               |

Dependencies
------------

No dependencies.


Example Inventory File
----------------------
[local]
localhost


Example Playbook
----------------

---

- hosts: local
  vars_file:

      - ./path/secure.yml

  roles:
  
    - /path/ec2_create
    
...


## Contributing

Issues, feature requests, ideas are appreciated and can be posted in the Issues section.


Author Information
------------------
LinkedIn: https://www.linkedin.com/in/bobby-singh-4321791a7/
Email Id: bharat8249@gmail.com

