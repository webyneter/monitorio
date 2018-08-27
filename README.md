# monitorio

Customizes https://github.com/vegasbrianc/prometheus


## Operating the Stack

### Locally

#### Prerequisites

* [Ansible](https://docs.ansible.com/ansible/latest/installation_guide/intro_installation.html)

#### Commands

```bash
ansible-playbook --inventory ./ansible/environments/local/ ./ansible/local.yml
```


### Remotely

#### Staging

You should never do that.


#### Production

You should never do that.


## Tips & Tricks

### Ansible

```bash
# https://docs.ansible.com/ansible/2.4/vault.html

# Editing Encrypted Files
ansible-vault edit ./ansible/environments/staging/group_vars/all/999_secret.overrides.yml

# Viewing Encrypted Files
ansible-vault view ./ansible/environments/staging/group_vars/all/999_secret.overrides.yml
```
