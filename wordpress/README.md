# Create Simple Wordpress Server

This playbook is a one stop shop to configure Wordpress on a CentOS7 Server. Built/tested and used to create my site at blog.lottabytes.com running in GCP.

Make sure to add your IP address to the /etc/ansible/hosts file.

Execute with the following variables:
* db_name
* db_user
* db_pass
* db_root
* db_root_pass
* wp_salt_phrase

Example: 
```
ansible-playbook simple-wordpress.yml --extra-vars "db_name=wordpress db_user=u_wp db_pass=Password1! db_root_pass=Password2! wp_salt_phrase=Salt-Phase-1234"
```
post install you can easily run the EFF CertBot to get a valid SSL certificate
```
./certbot --apache
```
then follow the prompts...

You should be able to access your site via https://fqdn or IP
