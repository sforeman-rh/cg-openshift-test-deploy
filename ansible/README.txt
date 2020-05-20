This ansible playbook was written to run on your local host, and will create Operator subscriptions on the remote host specified in the hosts file. Currently, this points to my test server with my SSL authentication info, so be careful and update it for your own uses ;)

I will try to add dependency resolution to this automation as well. For now, here are the dependencies I have:
localhost:
Ansible Kubernetes Collection (Requires Ansible 2.9+)
ansible-galaxy collection install community.kubernetes

remote host:
Ansible Kubernetes Collection (Requires Ansible 2.9+)
ansible-galaxy collection install community.kubernetes

Python openshift library
yum install python2-pip
pip install openshift

Execution command on localhost:
ansible-playbook ServiceMeshSub.yaml -i hosts