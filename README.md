# my-playbook

Ansible playbook for deploying my applications

```
# install roles
ansible-galaxy install -r requirements.yml

# dev
ansible-playbook site.yml -i inventory.dev

# prod
ansible-playbook site.yml -i inventory.dev
```
