# Create Simple Wordpress Server

This playbook is a one stop shop to configure Wordpress on a CentOS7 Server. Built/tested and used to create my site at blog.lottabytes.com running in GCP.

Make sure to add your IP address to the /etc/ansible/hosts file.

Execute with the following variables:
1. db_name
2. db_user
3. db_pass
4. db_root
5. db_root_pass
6. wp_salt_phrase

Example: 
```
ansible-playbook simple-wordpress.yml --extra-vars "db_name=wordpress db_user=u_wp db_pass=Password1! db_root_pass=Password2! wp_salt_phrase=Salt-Phase-1234"
```
