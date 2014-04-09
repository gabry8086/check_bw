Bandwidth Calculator


A simple bash script to calculate input or output bandwidth usage based on a snmp data

Based on Cisco Document ID: 8141

- Requirements: Bc, snmpwalk 

 refer to -> 1.3.6.1.2.1.31.1.1.1.1 OID to find out your interface name/number and associate to your right 
 ifOutOctets and ifInOctets OID 

 You can also customize data polling time according to your needs 

usage example: 
[root@something ~]#./check_bw.sh -H ipaddress -b 30 -v 2c -m input -C community_name -i interfacename

I've Personally tested it only on my Nagios 3.x environment
And under those OS's (Centos 5 and 6, Debian 7, FreeBSD 9.1 and ASA 8.4 )

it actually supports only snmp version 1 and 2c, 
I will add version 3 support as soon as i can 

further explanations inside the script.
