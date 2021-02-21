kubernetes_master
=========

A master node is a node which controls and manages a set of worker nodes (workloads runtime) and resembles a cluster in Kubernetes. 

This role is created to configure Kubernetes Master on top of AWS linux  Instance and local host.

Requirements
------------

- Deployment environment must have Ansible 2.9.0+
- Master and nodes must have passwordless SSH access
- Boto3 for aws ec2 instances 



Dependencies
------------

None

About Master Node
------------

A master node has the following components to help manage worker nodes:

- Kube-APIServer, which acts as the frontend to the cluster. All external communication to the cluster is via the API-Server.
- Kube-Controller-Manager, which runs a set of controllers for the running cluster. The controller-manager implements governance across the cluster.
Etcd, the cluster state database.
- Kube Scheduler, which schedules activities to the worker nodes based on events occurring on the etcd. It also holds the nodes resources plan to determine the proper action for the triggered event. For example the scheduler would figure out which worker node will host a newly scheduled POD.


Example Playbook
----------------

To use this role in your own playbook, refer the following example:


       - hosts: "tag_Name_Kubernetes_master"
         vars_files:
                - ./secure.yml
         roles:
             - role: kubernetes_master

License
-------

BSD

Author Information
------------------

LinkedIn: https://www.linkedin.com/in/bobby-singh-4321791a7/
Email Id: bharat8249@gmail.com

