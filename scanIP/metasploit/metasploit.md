# Metasploit

***
## open
```shell
bob@kali:~/Reference/Hack/kalitools$ msfconsole
[-] ***rting the Metasploit Framework console...-
[-] * WARNING: No database support: No database YAML file
[-] ***
[*] Starting the MetasploiT Framework console...-
...
```

## portscan
```shell
msf5 > search portscan

Matching Modules
================

   #  Name                                              Disclosure Date  Rank    Check  Description
   -  ----                                              ---------------  ----    -----  -----------
   1  auxiliary/scanner/http/wordpress_pingback_access                   normal  Yes    Wordpress Pingback Locator
   2  auxiliary/scanner/natpmp/natpmp_portscan                           normal  Yes    NAT-PMP External Port Scanner
```

## use portscan 
```shell
msf5 > use  auxiliary/scanner/portscan/syn  
msf5 auxiliary(scanner/portscan/syn) > info

       Name: TCP SYN Port Scanner
     Module: auxiliary/scanner/portscan/syn
    License: Metasploit Framework License (BSD)
       Rank: Normal

Provided by:
  kris katterjohn <katterjohn@gmail.com>
  ...

```

## get portscan options
```shell
msf5 auxiliary(scanner/portscan/syn) > options

Module options (auxiliary/scanner/portscan/syn):

   Name       Current Setting  Required  Description
   ----       ---------------  --------  -----------
   BATCHSIZE  256              yes       The number of hosts to scan per set
   DELAY      0                yes       The delay between connections, per thread, in milliseconds
   INTERFACE                   no        The name of the interface
   JITTER     0                yes       The delay jitter factor (maximum value by which to +/- DELAY) in milliseconds.
   PORTS      1-10000          yes       Ports to scan (e.g. 22-25,80,110-900)
   RHOSTS                      yes       The target address range or CIDR identifier
   SNAPLEN    65535            yes       The number of bytes to capture
   THREADS    1                yes       The number of concurrent threads
   TIMEOUT    500              yes       The reply read timeout in milliseconds
```

## set ports
```shell
msf5 auxiliary(scanner/portscan/syn) > set ports 1-65535
ports => 1-65535
```

## set rhosts
```shell
msf5 auxiliary(scanner/portscan/syn) > set rhosts 10.0.2.15
rhosts => 10.0.2.15
```

