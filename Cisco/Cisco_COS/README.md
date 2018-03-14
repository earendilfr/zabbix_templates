# Template for Cisco COS

## Requirment

This template use a perl script to retrieve the index to pool.
You need to install the script __cisco.cos.discovery__ in the discovery directory and have the following package installed on your distribution:

* For RHEL distribution
 - perl-Net-SNMP
 - perl-JSON
 - perl-Pod-Usage
 - perl-Data-Dumper
 - perl-Getopt-Long

Warning, you need to check the mode of the script (it should be executable by the zabbix user) and, to avoid issue with the selinux right, you should have the profile __zabbix_script_exec_t__


## Function

To use this template, you should add it to the profile for your router with the following MACRO defined:

- QOSNAME_INPUT: a regexp that match the policy-map for input COS
- CMNAME_INPUT: a regexp that match the class map of your COS

- QOSNAME_OUTPUT: a regexp that match the policy-map for output COS
- CMNAME_OUTPUT: a regexp that match the class map of your COS


