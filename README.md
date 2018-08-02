# monitorio

A snapshot fork of https://github.com/vegasbrianc/prometheus with a few improvements


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
ansible-vault edit ./ansible/environments/staging/group_vars/all/secret.overrides.yml

# Viewing Encrypted Files
ansible-vault view ./ansible/environments/staging/group_vars/all/secret.overrides.yml
```

### Generating SSH public-private key pair for CI

```bash
mkdir -p ./.ssh/

# N.B. For seamless CI experience, no passphrase is being set.
ssh-keygen \
    -q \
    -b 4096 \
    -t rsa \
    -N "" \
    -C id_rsa \
    -f ./.ssh/id_rsa

ssh-copy-id -i ./.ssh/id_rsa -p <port> <user@host>
```
