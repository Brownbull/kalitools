# Enumeration

***
```shell
ifconfig
# get inet and use it as target on netdiscover
netdiscover -r 10.0.2.0/24
```

# Target
sitiodepruebas.org
165.22.34.38

# Pentesting
Run Nessus Basic Network Scan
```shell
nmap -T4 -p- 165.22.34.38
    Nmap scan report for 165.22.34.38
    Host is up (0.11s latency).
    Not shown: 65532 filtered ports
    PORT    STATE SERVICE
    22/tcp  open  ssh
    80/tcp  open  http
    443/tcp open  https
# get open ports
# use them
nmap -A -T4 -p22,80,443 165.22.34.38
    PORT    STATE    SERVICE  VERSION
    22/tcp  filtered ssh
    80/tcp  open     http     Apache httpd 2.4.29 ((Ubuntu))
    |_http-server-header: Apache/2.4.29 (Ubuntu)
    |_http-title: plantillas web
    443/tcp open     ssl/http Apache httpd 2.4.29 ((Ubuntu))
    |_http-server-header: Apache/2.4.29 (Ubuntu)
    |_http-title: plantillas web
    | ssl-cert: Subject: commonName=sitiodepruebas.org
    | Subject Alternative Name: DNS:sitiodepruebas.org
    | Not valid before: 2019-10-15T03:28:37
    |_Not valid after:  2020-01-13T03:28:37
    |_ssl-date: TLS randomness does not represent time
    | tls-alpn: 
    |   http/1.1
nikto -h 165.22.34.38
dirbuster
# paste url with port like this
# http://165.22.34.38:80/
# then select /usr/share/wordlists/dirbuster/directory-list-lowercase-2.3-small.txt
# put multiple file extensions
# php, asa, sql, zip, tar, pdf, txt, bak
# Start

# CURL
>curl --head 165.22.34.38
```