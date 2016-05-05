# mkl-install-playbook

1. install the mkl install role

```
[sudo] ansible-galaxy install -r requirements.yml --ignore-errors
```

2. Update the hosts variable in the sample [cdh.yml](cdh.yml) file.
```
---
- hosts: YOURHOSTS
  become: yes
  become_user: root
  roles:
  - { role: mkl-install-role } 
```

3. Run playbook
```
ansible-playbook mkl.yml
```
