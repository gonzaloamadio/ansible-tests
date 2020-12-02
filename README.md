# ansible-tests
Some tests with ansible infra automation tool

# Install ansible

```
$ sudo apt-get update
$ sudo apt-get install software-properties-common
$ sudo apt-add-repository ppa:ansible/ansible
$ sudo apt-get update
$ sudo apt-get install ansible
```

Install dependencies used in the project
```
$ sudo apt-get install python-jmespath
```

# Usage

Edit ansible config as needed: /etc/ansible/ansible.cfg

For example:
```
inventory = /path/to/repo/inventory01.yml
```

# Some commands

```
ansible --version

# An inventory represents the machines that Ansible will manage. This command should show all the inventory machines.
ansible --list-hosts all
# Or list only a group (a group is created with brackets)
ansible --list-hosts group_name_here

# free -m
ansible -m shell -a 'free -m' all

# Run ls command on all machines
ansible -m command -a "ls" all
# Execute ls on all machines with a playbook
ansible-playbook playbooks/ls-all.yml
```


# References

LOT OF playbook examples: https://www.middlewareinventory.com/blog/ansible-playbook-example/

https://linuxhint.com/ansible-tutorial-beginners/

Read json file and use as variables in playbook
https://www.middlewareinventory.com/blog/ansible-playbook-read-json-file/

