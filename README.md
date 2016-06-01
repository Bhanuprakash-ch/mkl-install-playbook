# mkl-install-playbook

-0. install required packages for ansible
```
sudo yum install wget libffi-devel python-devel python-pip python-setuptools gmp-devel
```

-1. Install ansible
```
sudo pip install -U ansible==1.9.4
```

-2. Clone and cd into repository
```
git clone https://github.com/trustedanalytics/mkl-install-playbook.git && cd mkl-install-playbook
```

-3. Remove old mkl install role.
```
sudo ansible-galaxy remove mkl-install-role
```

-4. Install the mkl-install role.

```
sudo ansible-galaxy install -r requirements.yml
```

-5. Update the hosts file [hosts](hosts) with the hostnames that need mkl.
```
[YOURHOSTS]
localhost
```

-6. Run playbook
```
ansible-playbook --inventory hosts mkl.yml
```
