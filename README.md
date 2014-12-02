# neutron-net-setup

### netsetup.sh
- Creates a provider net/subnet *public/public-subnet*
- Creates a tenant net/subnet *private/private-subnet*
- Creates a router *public-private*
- Sets a router gateway
- Adds an interface between the router and the tenant subnet
- Adds security group rules for ingress/egress ssh, and ingress icmp traffic

### netsetup-plus.sh
- Performs all of the actions of **netsetup.sh**
- Creates Keystone tenants/users required for testing with CloudCafe
- Downloads cirros-0.3.2 and cirros-0.3.3 images and uploads them to Glance
- Creates an additional security group required for testing with CloudCafe

### sanity-check.sh
- Boots a VM using the cirros-0.3.3 image
- Creates a floatingip and associates it with the VM
- Attempts to ping the floating IP (*exit on failure*)
- Cleans up the environment if ping was successful
