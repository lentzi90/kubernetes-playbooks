# kubernetes-playbooks

This repository contains ansible playbooks and roles for kubernetes.

The playbook `deploy_kubernetes.yml` can be used to set up a cluster:
```
ansible-playbook -i inventory deploy_kubernetes.yml
```

The inventory should look something like this:
```
[clients]
master

[workers]
worker

[masters]
master

[nodes]
master
worker
```

## TODO

- Support multiple masters (HA)
- Add playbook for scaling up
- Add playbook(s) for adding basic komponents like [cert-manager](https://github.com/jetstack/cert-manager) and ingress controller.
