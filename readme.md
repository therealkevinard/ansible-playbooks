
- [rke-k8s-setup](./rke-k8s-setup/rke-k8s-setup.yaml)  
Installs **local** tooling for working with RKE Kubernetes  
    - **Only tested on Ubuntu 18.04 / linux-amd64** 
    - uses voodoo magic to find latest versions via `github api | jq`  
    - Toolkit 
        - [Kubectl](https://kubernetes.io/docs/reference/kubectl/overview/) (with bash completion) 
            - If this is the first install, you'll need to init `~/.kube/config` yourself. 
        - [Helm](https://helm.sh/) (with bash completion)
        - [Kubens/Kubectx](https://github.com/ahmetb/kubectx/), 
            - installs binaries as `kns` and `kctx` so they don't clash with `kubectl` tab-complete :) 
        - [Kompose](https://kompose.io/) (with bash completion)
        - [Skaffold](https://skaffold.dev/) (with bash completion)
        - [Rancher CLI](https://github.com/rancher/cli)

- [git-backup-apps](./git-backup-apps)  
A routine for rebuilding legacy production apps in gitops repos. 
    - Prefers inventory-specific makefiles. If a Makefile is found in remote_root ([ref default](./git-backup-apps/create-default-mk.yml)), 
    it will run the rebuild_repo target.
    - If the Makefile check fails, will try attempt fallbacks for generic/routine cms'  