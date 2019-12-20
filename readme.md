
- [rke-k8s-setup](./rke-k8s-setup/rke-k8s-setup.yaml)  
    - **Only tested on Ubuntu 18.04 / linux-amd64** 
    - Installs tools for working with an rke k8s cluster.  
    - Kubectl, Helm, Kubens/Kubectx, Kompose, Rancher CLI; bash completion form kubectl, helm, and kompose
    - uses voodoo magic to find latest versions via `github api | jq`  
  
