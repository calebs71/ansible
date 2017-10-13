#Install and configures net-smnp on PhotonOS

Runsafe (can be run as many times as desired without negative consequences) playbook that installs and configures net-snmp and creates a SNMP v3 read-only user for monitoring.

Following variables are used for SNMP configuration with examples:
* sysLocation - US01
* sysContact - user@domain.com
* sysName - myhostname

The following values are optional:
* snmpProto - Defaults to udp, can be over-ridden to tcp
* snmpPort - Defaults to 161, can be over-ridden

Variables for the Read-Only SNMP v3 user
* authPass - Authentication Password
* privPass - Privacy Password
* snmpUser - Username

The following values are optional:
* authType - Defaults to SHA, can be over-ridden to MD5
* privType - Defauls to AES, can be over-ridden to DES 

Note: This playbook will not change the SNMP User if the passwords don't match. It will only create the user if it doesn't currently exist.

Example:
```
ansible-playbook configure-snmp.yml -u root -k --extra-vars "sysLocation=us01 sysContact=caleb@lottabytes.com sysName=photontest authPass=1b3d5f7h privPass=1b3d5f7h snmpUser=zenoss"
```
