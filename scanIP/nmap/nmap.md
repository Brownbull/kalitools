# NMAP
- [NMAP](#NMAP)
  - [Execute](#Execute)
    - [scan ports in an IP](#scan-ports-in-an-IP)
    - [scan TCP ports T4 speed](#scan-TCP-ports-T4-speed)
    - [scan All and all ports](#scan-All-and-all-ports)
    - [scan UDP](#scan-UDP)
    - [scan cyphers](#scan-cyphers)
***
## Execute

### scan ports in an IP
```shell
root@kali:~/Reference/hack/kalitools# nmap -sn 10.0.2.15/24
Starting Nmap 7.70 ( https://nmap.org ) at 2019-11-03 19:31 CST
Nmap scan report for 10.0.2.2
Host is up (0.00013s latency).
MAC Address: 52:54:00:12:35:02 (QEMU virtual NIC)
Nmap scan report for 10.0.2.3
Host is up (0.00011s latency).
MAC Address: 52:54:00:12:35:03 (QEMU virtual NIC)
Nmap scan report for 10.0.2.4
Host is up (0.00011s latency).
MAC Address: 52:54:00:12:35:04 (QEMU virtual NIC)
Nmap scan report for 10.0.2.15
Host is up.
Nmap done: 256 IP addresses (4 hosts up) scanned in 2.10 seconds
```
### scan TCP ports T4 speed
```shell
root@kali:~/Reference/hack/kalitools# nmap -T4 10.0.2.15
Starting Nmap 7.70 ( https://nmap.org ) at 2019-11-03 19:32 CST
Nmap scan report for 10.0.2.15
Host is up (0.0000040s latency).
Not shown: 998 closed ports
PORT    STATE SERVICE
22/tcp  open  ssh
111/tcp open  rpcbind

Nmap done: 1 IP address (1 host up) scanned in 0.20 seconds
```

### scan All and all ports
```shell
root@kali:~/Reference/hack/kalitools# nmap -sn 10.0.2.15/24
Starting Nmap 7.70 ( https://nmap.org ) at 2019-11-03 19:31 CST
Nmap scan report for 10.0.2.2
Host is up (0.00013s latency).
MAC Address: 52:54:00:12:35:02 (QEMU virtual NIC)
Nmap scan report for 10.0.2.3
Host is up (0.00011s latency).
MAC Address: 52:54:00:12:35:03 (QEMU virtual NIC)
Nmap scan report for 10.0.2.4
Host is up (0.00011s latency).
MAC Address: 52:54:00:12:35:04 (QEMU virtual NIC)
Nmap scan report for 10.0.2.15
Host is up.
Nmap done: 256 IP addresses (4 hosts up) scanned in 2.10 seconds
root@kali:~/Reference/hack/kalitools# nmap -T4 10.0.2.15
Starting Nmap 7.70 ( https://nmap.org ) at 2019-11-03 19:32 CST
Nmap scan report for 10.0.2.15
Host is up (0.0000040s latency).
Not shown: 998 closed ports
PORT    STATE SERVICE
22/tcp  open  ssh
111/tcp open  rpcbind

Nmap done: 1 IP address (1 host up) scanned in 0.20 seconds
root@kali:~/Reference/hack/kalitools# nmap -T4 -A -p- 10.0.2.15
Starting Nmap 7.70 ( https://nmap.org ) at 2019-11-03 19:34 CST
Nmap scan report for 10.0.2.15
Host is up (0.000030s latency).
Not shown: 65533 closed ports
PORT    STATE SERVICE VERSION
22/tcp  open  ssh     OpenSSH 7.9p1 Debian 10 (protocol 2.0)
| ssh-hostkey: 
|   2048 fe:f8:4e:ad:f6:42:bf:38:17:7d:8c:09:4f:64:c6:0d (RSA)
|   256 b8:eb:42:60:44:7b:84:8c:8c:da:09:15:9c:d6:3c:80 (ECDSA)
|_  256 69:83:65:58:48:ae:64:05:04:bf:41:7e:c8:b8:e6:b7 (ED25519)
111/tcp open  rpcbind 2-4 (RPC #100000)
| rpcinfo: 
|   program version   port/proto  service
|   100000  2,3,4        111/tcp  rpcbind
|_  100000  2,3,4        111/udp  rpcbind
Device type: general purpose
Running: Linux 3.X
OS CPE: cpe:/o:linux:linux_kernel:3
OS details: Linux 3.7 - 3.10
Network Distance: 0 hops
Service Info: OS: Linux; CPE: cpe:/o:linux:linux_kernel

OS and Service detection performed. Please report any incorrect results at https://nmap.org/submit/ .
Nmap done: 1 IP address (1 host up) scanned in 10.28 seconds
```

### scan UDP
```shell
root@kali:~/Reference/hack/kalitools# nmap -sU -T4 10.0.2.15
Starting Nmap 7.70 ( https://nmap.org ) at 2019-11-03 19:42 CST
Nmap scan report for 10.0.2.15
Host is up (0.0000050s latency).
Not shown: 998 closed ports
PORT    STATE         SERVICE
68/udp  open|filtered dhcpc
111/udp open          rpcbind

Nmap done: 1 IP address (1 host up) scanned in 1.34 seconds
```
### scan cyphers
```shell
root@kali:~/Reference/hack/kalitools# nmap -p 443 --script=ssl-enum-ciphers tesla.com
Starting Nmap 7.70 ( https://nmap.org ) at 2019-11-03 19:45 CST
Starting Nmap 7.70 ( https://nmap.org ) at 2019-11-03 19:45 CST
Nmap scan report for tesla.com (209.133.79.61)
Host is up (0.050s latency).

PORT    STATE SERVICE
443/tcp open  https
| ssl-enum-ciphers: 
|   TLSv1.0: 
|     ciphers: 
|       TLS_ECDHE_RSA_WITH_AES_128_CBC_SHA (secp256r1) - A
|       TLS_ECDHE_RSA_WITH_AES_256_CBC_SHA (secp256r1) - A
...
```
