# L3LS_Provisioning
Used to create simple L3LS configuration for containerlab quickly.

Utilizes roles leafs, spines, and global.

Currently using ansible vault and the file group_vars/all.yml will need to be deleted and recreated with the proper credentials.  Below is an example of what that file would look like.

  * eos_api:
  * host: '{{ inventory_hostname }}'
  * username: 
  * password: 
  * authorize: true
  * use_ssl: yes
  * transport: eapi
  * validate_certs: false

All tasks and templates for leafs are located under the leafs directory.
All tasks and templates for spines are located under the spines directory.
All tasks and templates for global are located under the global directory.

You will need to modify the inventory file to include your switches as well as change the host_vars/ files to match your inventory IP's.
