* vagrant files to create virtualbox machines
* ansible playbook to bootstrap cluster, install cni, metric server and dashboard

```bash
# this will create the vms
vagrant init

# add vm to local ssh config
vagrant ssh-config master >> ~/.ssh/config
vagrant ssh-config worker1 >> ~/.ssh/config
vagrant ssh-config worker2 >> ~/.ssh/config

# run playbook to install and initialize cluster
ansible-playbook -i inventory.ini playbook.yaml
```
