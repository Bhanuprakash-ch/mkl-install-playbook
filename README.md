# mkl-install-playbook

1. Install the mkl-install role.

```
[sudo] ansible-galaxy install -r requirements.yml --ignore-errors
```

2. Update the hosts file [hosts](hosts) with the hostnames that need mkl.
```
[YOURHOSTS]
localhost
```

3. Run playbook
```
ansible-playbook --inventory hosts mkl.yml
```
