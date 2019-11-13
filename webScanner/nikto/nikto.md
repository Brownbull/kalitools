# Nikto

***
## Scan 
```shell
nikto -h https://sitiodepruebas.org/
- Nikto v2.1.6
---------------------------------------------------------------------------
+ Target IP:          165.22.34.38
+ Target Hostname:    sitiodepruebas.org
+ Target Port:        443
---------------------------------------------------------------------------
+ SSL Info:        Subject:  /CN=sitiodepruebas.org
                   Ciphers:  ECDHE-RSA-CHACHA20-POLY1305
                   Issuer:   /C=US/O=Let's Encrypt/CN=Let's Encrypt Authority X3
+ Start Time:         2019-11-12 15:31:44 (GMT-6)
---------------------------------------------------------------------------
+ Server: Apache/2.4.29 (Ubuntu)
+ The anti-clickjacking X-Frame-Options header is not present.
+ The X-XSS-Protection header is not defined. This header can hint to the user agent to protect against some forms of XSS
+ The site uses SSL and the Strict-Transport-Security HTTP header is not defined.
+ The site uses SSL and Expect-CT header is not present.
+ The X-Content-Type-Options header is not set. This could allow the user agent to render the content of the site in a different fashion to the MIME type
+ No CGI Directories found (use '-C all' to force check all possible dirs)
+ Apache/2.4.29 appears to be outdated (current is at least Apache/2.4.37). Apache 2.2.34 is the EOL for the 2.x branch.
+ Server may leak inodes via ETags, header found with file /, inode: 3514, size: 5902d9f4f2569, mtime: gzip
+ The Content-Encoding header is set to "deflate" this may mean that the server is vulnerable to the BREACH attack.
+ Allowed HTTP Methods: HEAD, GET, POST, OPTIONS 
+ OSVDB-3268: /css/: Directory indexing found.
+ OSVDB-3092: /css/: This might be interesting...
+ OSVDB-3268: /images/: Directory indexing found.
+ OSVDB-3233: /icons/README: Apache default file found.
+ 7785 requests: 0 error(s) and 13 item(s) reported on remote host
+ End Time:           2019-11-12 20:00:46 (GMT-6) (16142 seconds)
---------------------------------------------------------------------------
+ 1 host(s) tested

```