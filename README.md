# Ansible Role: K8s RKE


An ansible role that setup kubernetes cluster with rke on rhel/centos/fedora and debian/ubuntu. 

![Ansible Galaxy](https://github.com/BasisTI/ansible_rke/workflows/Ansible%20Galaxy/badge.svg)

## Tags:
## Variables:

* `rke_kubernetes_version`: `v1.19.3-rancher1-1` - Map the RKE kubernetes image version across the selection to the kubernetes version.



* `rke_version`: `v1.2.1` - Defines rke version.



* `rke_binary_url`: `"https://github.com/rancher/rke/releases/download/{{ rke_version }}/rke_linux-amd64"` - Defines rke binary url download.



* `rke_user`: `rke` - User that will be used to connect on nodes during the installation proccess.



* `rke_node`: `"{{ groups['masters'] | first }}"` - Node that will be used to deploy cluster using RKE.



* `rke_cluster_network_cidr`: `'10.42.0.0/16'` - CIDR pool used to assign IP addresses to pods in the cluster.



* `rke_service_network_cidr`: `'10.43.0.0/16'` - This is the virtual IP address that will be assigned to services created on Kubernetes.


## License
Mit



Documentation generated using: [Ansible-autodoc](https://github.com/AndresBott/ansible-autodoc)

