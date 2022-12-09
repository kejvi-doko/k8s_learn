## Hardware Architecture ##

- Master Node 10.211.55.3
- Worker1 Node 10.211.55.4
- Worker2 Node 10.211.55.5

## Configure Kubernetes Cluster

```shell
ansible-playbook -i k8s-cluster/hosts k8s-cluster/install-kube-prereq.yml --extra-vars "ansible_sudo_pass=111111"
ansible-playbook -i k8s-cluster/hosts k8s-cluster/install-kube-components.yml --extra-vars "ansible_sudo_pass=111111"
ansible-playbook -i k8s-cluster/hosts k8s-cluster/master.yml --extra-vars "ansible_sudo_pass=111111"
ansible-playbook -i k8s-cluster/hosts k8s-cluster/worker.yml --extra-vars "ansible_sudo_pass=111111"
ansible-playbook -i k8s-cluster/hosts k8s-cluster/install-pod-network-addon.yml --extra-vars "ansible_sudo_pass=111111"
```