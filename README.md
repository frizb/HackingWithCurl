# Hacking With cURL
A list of examples and references of hacking with Bash and the Curl command.

## What the heck is cURL?
cURL is short for "Client URL" and is a computer software project providing a library (libcurl) and command-line tool (curl) first released in 1997. It is a free client-side URL transfer library that supports the following protocols:
`Cookies, DICT, FTP, FTPS, Gopher, HTTP/1, HTTP/2, HTTP POST, HTTP PUT, HTTP proxy tunneling, HTTPS, IMAP, Kerberos, LDAP, POP3, RTSP, SCP, and SMTP`

## cURL GET parameters
HTTP GET variables can be set by adding them to the URL.
Here is a simple get request example:
```

```

## cURL POST parameters
HTTP POST variables can be set using the -d (--data) parameter.  
Here is a simple login test example:  
```
curl --data "email=test@test.com&password=test" http://10.10.10.10/login.php
```
## cURL COOKIEs

##


## Attacking a Login Form with cURL
```
curl --data "email=test@test.com&password=test" http://10.10.10.10/login.php
```

## Creating new Users with cURL

```

```
