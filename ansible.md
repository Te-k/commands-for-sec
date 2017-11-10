# Ansible

**Test connection as root**
```bash
$ ansible all -m ping -u USER --ask-become-pass
```

**Run command directly**
```bash
$ ansible all -s -m shell -a 'apt-get install nginx'
```

**Run playbook and ask for sudo password**
```bash
$ ansible-playbook -s main.yml -K
```
