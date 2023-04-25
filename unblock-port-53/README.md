## Unblock Port 53

By default port 53 is used by systemd-resolved on Ubuntu, it means that you can't run your own DNS server. This playbook removes this limitation by:
- **setting Quad9 as the DNS server** (9.9.9.9),
- disabling DNS stub listener.

## Running the playbook
```ansible
ansible-pull -U https://github.com/xelofan/ansible-projects unblock-port-53/unblock-port-53.yml 
```

**You'll have to reboot to apply the changes.**