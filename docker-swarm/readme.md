# Docker Swarm + Keepalived VIP playbook

## TODO:
- Ability to add nodes as workers not just managers

## Usage

### Clone the repo
```bash
git clone https://github.com/Xelofan/ansible && \
cd ansible/docker-swarm
```

### Create a `hosts` file and fill it up with your nodes' IPs

*ansible/docker-swarm/hosts*
```bash
10.0.1.11
10.0.1.12
10.0.1.13
```

### Change your desired VIP and address pool in the main `playbook.yml` file

*ansible/docker-swarm/playbook.yml*
```yaml
 # ...
  vars:
    address_pool: "172.22.0.0/24"
    vip: "10.0.1.10"
 # ...
```