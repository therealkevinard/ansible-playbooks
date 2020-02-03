- [git-backup-apps](./git-backup-apps)  
A routine for rebuilding legacy production apps in gitops repos. 
    - Prefers inventory-specific makefiles. If a Makefile is found in remote_root ([ref default](./git-backup-apps/create-default-mk.yml)), 
    it will run the rebuild_repo target.
    - If the Makefile check fails, will try attempt fallbacks for generic/routine cms'  