#!/bin/bash

vagrant ssh-config master >> ~/.ssh/config
vagrant ssh-config worker1 >> ~/.ssh/config
vagrant ssh-config worker2 >> ~/.ssh/config

ansible-playbook -i inventory.ini playbook.yaml
