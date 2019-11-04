# Whatweb

***
## execute
```shell
root@kali:~/Reference/hack/kalitools# whatweb -v teesla.com
```

## results
```shell
WhatWeb report for http://teesla.com
Status    : 200 OK
Title     : <None>
IP        : 199.59.242.153
Country   : UNITED STATES, US

Summary   : HTTPServer[openresty], HTML5, Script[text/javascript], UncommonHeaders[x-adblock-key]

Detected Plugins:
[ HTML5 ]
        HTML version 5, detected by the doctype declaration 


[ HTTPServer ]
        HTTP server header string. This plugin also attempts to 
        identify the operating system from the server header. 

        String       : openresty (from server string)

[ Script ]
        This plugin detects instances of script HTML elements and 
        returns the script language/type. 

        String       : text/javascript

[ UncommonHeaders ]
        Uncommon HTTP server headers. The blacklist includes all 
        the standard headers and many non standard but common ones. 
        Interesting but fairly common headers should have their own 
        plugins, eg. x-powered-by, server and x-aspnet-version. 
        Info about headers can be found at www.http-stats.com 

        String       : x-adblock-key (from headers)

HTTP Headers:
        HTTP/1.1 200 OK
        Server: openresty
        Date: Mon, 04 Nov 2019 00:45:57 GMT
        Content-Type: text/html; charset=UTF-8
        Transfer-Encoding: chunked
        Connection: close
        X-Adblock-Key: MFwwDQYJKoZIhvcNAQEBBQADSwAwSAJBANDrp2lz7AOmADaN8tA50LsWcjLFyQFcb/P2Txc58oYOeILb3vBw7J6f4pamkAQVSQuqYsKx3YzdUHCvbVZvFUsCAwEAAQ==_AeCRSaC8NXJ8OKu0UWTbk2NOaHIRIi7h6O+64sRmmpF4CNX6ShvC+al0svXFANBd+k/XR8XZSe2RR14W2U9Mtw==
```
