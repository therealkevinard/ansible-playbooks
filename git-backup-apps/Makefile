inventory=/home/kevin/Workspaces/technology-director/kubernetes-migration/tools/node-inventory-csv-parser/parsed/inventory.yml
varsfile=.local/run_vars.yml

host_filter=massariwooddancecom
#host_filter=wordpress:&digitalocean
#host_filter=wordpress:!digitalocean # all wp sites, not on digital ocean
extra_args=-v

run:
	ansible-playbook \
		--inventory $(inventory) \
		--extra-vars "@$(varsfile)" \
		--extra-vars '{"inventory_host": "$(host_filter)"}' \
		$(extra_args) ./gitops-migrations.yml

inventory:
	ansible-inventory -i $(inventory) --graph