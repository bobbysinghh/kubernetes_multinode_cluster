kubernetes_slave
=========


A Kubernetes cluster consists of a set of worker machines, called nodes, that run containerized applications. Every cluster has at least one worker node.
This role is created to configure Kubernetes slave  on top of AWS linux  Instance.


Requirements
------------

- Deployment environment must have Ansible 2.9.0+
- Master and nodes must have passwordless SSH access
- Boto3
 
Role Variables
--------------
 Give the value of `token` variable at start time

Dependencies
------------

None

About Worker Node
------------
- The worker node(s) host the Pods that are the components of the application workload. 
- The control plane manages the worker nodes and the Pods in the cluster.
- The node components run on every cluster node. These include:
container runtime: such as Docker, to execute containers on the node.
kubelet: executes containers (pods) on the node as dictated by the control plane’s scheduling, and ensures the
health of those pods (for example, by restarting failed pods).
kube-proxy: a network proxy/loadbalancer that implements the Service abstraction. It programs the iptables rules on
the node to redirect service IP requests to one of its registered backend pods.


Example Playbook
----------------

To use this role in your own playbook, refer the following examplie:


   - hosts: ["tag_Name_Kubernetes_Salve_1", "tag_Name_Kubernetes_Salve_2"]
     vars_files:
             - ./secure.yml
     vars_prompt:
         - name: token_join
          prompt: "Enter your token to join master"
          private: no
     roles:
        - role: kubernetes_slave

 
License
-------

BSD

Author Information
------------------

LinkedIn: https://www.linkedin.com/in/bobby-singh-4321791a7/
Email Id: bharat8249@gmail.com

