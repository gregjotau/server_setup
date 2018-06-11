
# Server setup

```
pip install ansible
# /ets/ansible/hosts contains inventory, else -i inventory_file is needed.
ansible-playbook playbook.yml
```

The `openstack.yml` playbook does the following:

* apt update and upgrade
* install git
* adds a private `deploy key` to .ssh folder, not sensitive info in any way shape or form
    * I do not bother to use `ansible vault`, since the key gives read access to one github repository
* clones a private git repo into /var/www/html