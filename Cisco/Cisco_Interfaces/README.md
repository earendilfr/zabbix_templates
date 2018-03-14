# Specific template for interface on Cisco devices

A template that could replace the Generic INterface template for Cisco devices.
it add:
- a retrieve a status off err-disabled of port (only for native port, not for subinterfaces)
- an IP address on a interface (if we have many IP addresses, only the first IP on the mib is retrieve)
- the list of the CDP neighbor on a port separated by the character |

## Installation

You need to install the script __cisco.if.cdp__ and __generic.if.ip__ in the externalscripts directory and have the following package installed on your distribution:

* For RHEL distribution
 - perl-Net-SNMP
 - perl-JSON
 - perl-Pod-Usage
 - perl-Data-Dumper
 - perl-Getopt-Long

Warning, you need to check the mode of the script (it should be executable by the zabbix user) and, to avoid issue with the selinux right, you should have the profile __zabbix_script_exec_t__
