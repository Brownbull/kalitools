# Whatweb

***
## execute
```shell
root@kali:~/Reference/hack/kalitools# whatweb -v tesla.com
```

## results
```shell
hatWeb report for http://tesla.com
Status    : 301 Moved Permanently
Title     : <None>
IP        : 209.133.79.61
Country   : UNITED STATES, US

Summary   : HTTPServer[BigIP], RedirectLocation[https://www.tesla.com/]

Detected Plugins:
[ HTTPServer ]
        HTTP server header string. This plugin also attempts to 
        identify the operating system from the server header. 

        String       : BigIP (from server string)

[ RedirectLocation ]
        HTTP Server string loca
        ...
```
