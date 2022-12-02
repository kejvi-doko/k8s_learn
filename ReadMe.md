## Hardware Architecture ##

- Master Node 10.211.55.3
- Worker1 Node 10.211.55.4
- Worker2 Node 10.211.55.5
- Worker3 Node 10.211.55.6

## Create Certificate 

```shell
ssh-keygen -b 4096 -t rsa
```

## Intial Setup

## Configure non-root users

Run this command `ansible-playbook -i k8s-cluster/hosts k8s-cluster/initial-setup.yml --extra-vars "ansible_sudo_pass=yourPassword"`

## Configure non-root users

Run this command `ansible-playbook -i k8s-cluster/hosts k8s-cluster/install-kube-components.yml --extra-vars "ansible_sudo_pass=yourPassword"`