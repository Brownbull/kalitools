# Nessus

***
## Setup
- [Nessus](#nessus)
  - [Setup](#setup)
  - [Start](#start)
  - [Restart](#restart)
    - [on linux](#on-linux)
      - [FAST](#fast)
      - [FULL](#full)
## Start
```shell
/etc/init.d/nessusd start
```
Open browser on
https://kali8834

## Restart
### on linux
#### FAST
```shell
su root
service nessusd stop
/opt/nessus/sbin/nessusd -R 
service nessusd start
```

#### FULL
```shell
su root
service nessusd stop
/opt/nessus/sbin/nessuscli fix --reset
/opt/nessus/sbin/nessuscli fetch --register ACTIVATION-CODE-HERE  
/opt/nessus/sbin/nessusd -R 
service nessusd start
```