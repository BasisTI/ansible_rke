# Ansible Role: Rancher Kubernetes Engine (RKE)


An ansible role that setup kubernetes cluster with rke on rhel/centos/fedora and debian/ubuntu. 

![Ansible Galaxy](https://github.com/BasisTI/ansible_rke/workflows/Ansible%20Galaxy/badge.svg)

## Tags:
## Variables:

* `kubernetes_supported_versions`: `{"v1.18.6": "v1.18.6-rancher1-1", "v1.17.9": "v1.17.9-rancher1-1", "v1.16.13": "v1.16.13-rancher1-1", "v1.15.12": "v1.15.12-rancher2-4"}` - Each version of RKE has a specific list of supported Kubernetes versions.

example: 


```yaml
kubernetes_supported_versions:
   v1.18.6: v1.18.6-rancher1-2
   v1.17.9: v1.17.9-rancher1-2
   v1.16.13: v1.16.13-rancher1-2
   v1.15.12: v1.15.12-rancher2-5
```

* `kubernetes_version`: `v1.18.6` - Specify the kubernetes version across kubernetes supported versions.



* `kubectl_version`: `"{{ kubernetes_version }}"` - Defines the kubectl version will be installed.



* `rke_kubernetes_version`: `"{{ kubernetes_supported_versions[kubernetes_version] }}"` - Map the RKE kubernetes image version across the selection to the kubernetes version.



* `rke_release_version`: `v1.1.6` - Defines rke version.



* `rke_binary_url`: `"https://github.com/rancher/rke/releases/download/{{ rke_release_version }}/rke_linux-amd64"` - Defines rke binary url download.



* `rke_node`: `"{{ groups.nodes | first }}"` - Node that will be used to deploy cluster using RKE.



* `rke_user`: `rke` - User that will be used to connect on nodes during the installation proccess.



* `rke_cluster_network_cidr`: `'10.42.0.0/16'` - CIDR pool used to assign IP addresses to pods in the cluster.



* `rke_service_network_cidr`: `'10.43.0.0/16'` - This is the virtual IP address that will be assigned to services created on Kubernetes.


## License
Apache-2.0



Documentation generated using: [Ansible-autodoc](https://github.com/AndresBott/ansible-autodoc)

