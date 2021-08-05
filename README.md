![gplv3](https://img.shields.io/badge/license-GPL%20v3.0-brightgreen.svg?style=flat-square)
![Maintenance](https://img.shields.io/maintenance/yes/2021?style=flat-square)

# ckaserer.users

The users role allows you to create users on your target node with random passwords.

First you need to install the role on the node from which you will execute ansible via

```
ansible-galaxy install ckaserer.users
```

---

## Create Users

The playbook below creates two users, `ckaserer` and `jdoe`, and sets a random password for each user stored in their home directory as `.password`.

```
- hosts: localhost
  tasks:
    - name: "Include ckaserer.users"
      include_role:
        name: "ckaserer.users"
        vars:
          users: 
            - ckaserer
            - jdoe
```
