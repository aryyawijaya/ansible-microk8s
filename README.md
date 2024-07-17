# ansible-microk8s
Set up mickrok8s (Kubernetes) using Ansible

## Set static IP
```bash
ansible-playbook -i <current_ip_vm/prefix_length>, set-static-ip.yaml -K -e "ip=<desired_static_ip>" -e "gateway=<gateway>" -e "hostname=<hostname_vm>"
```

## Set up microk8s
```bash
ansible-playbook -i inventory.ini set-up-microk8s.yaml -K
```

### Use kubectl command
SSH to VM
```bash
ssh <desired_static_ip>
```

Test kubectl command
```bash
kubectl version
```
![kubectl-version](https://github.com/aryyawijaya/ansible-microk8s/blob/main/docs/kubectl-version.png)
