# ansible_scripts

## node_info
```console
$ ansible-playbook node_info.yml
```

## ufw_status
```console
$ ansible-playbook ufw_status.yml
```

## update_upgrade
```console
$ ansible-playbook update_upgrade
```

## systemctl_status
```console
$ ansible-playbook systemctl_status \
  ---extra-vars "service_name=ssh"
```