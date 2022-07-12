# ansible_lihas_check_mk
Install check-mk from LiHAS Repositories, startup via systemd

Disables xinetd check_mk if running systemd

## Requirements

To run solo:
```
ansible-galaxy install -r requirements.yml
ansible-playbook -i localhost, check_mk.yml
```

## Dependencies

* lihas_common

## Variables
```
# add/remove check-mk-agent plugins via apt
X.config.check_mk.agent.plugins.add: []
X.config.check_mk.agent.plugins.remolve: []

```

## Example Playbook

```
---
- hosts: '*'
  role: lihas_check_mk
...
```
