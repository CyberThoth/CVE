#### Title: Clinic's Patient Management System 2.0 SQLi
#### Author: Ashish Kumar (https://www.linkedin.com/in/ashish-kumar-0b65a3184)
#### Date: 04.07.2022
#### Vendor: https://www.sourcecodester.com/users/tips23
#### Software: https://www.sourcecodester.com/php-clinics-patient-management-system-source-code
#### Version: 2.0
#### Reference: https://github.com/CyberThoth/CVE/blob/main/CVE/Clinic's%20Patient%20Management%20System/SQLi/POC.md

#### Description:
### The id parameter appears to be vulnerable to SQL injection attacks. The payload '+(select load_file('http://localhost/pms/index.php'))+' was submitted in the id parameter. This payload injects a SQL sub-query that calls MySQL's load_file function with a UNC file path that references a URL on an external domain. The application interacted with that domain, indicating that the injected SQL query was executed. The attacker can take administrator account control and also of all accounts on this system, also the malicious user can download all information about this system.

# Status: CRITICAL

### [+] Payloads:

``` 
Username: = admin' or '1'='1
Password: = Cyberthoth;)

```


## Proof and Exploit:
![image](https://github.com/CyberThoth/CVE/blob/5198ef2d56f9c818654bbe131c7f7e3055923f23/CVE/Clinic's%20Patient%20Management%20System/SQLi/1.png)

![image](https://github.com/CyberThoth/CVE/blob/5198ef2d56f9c818654bbe131c7f7e3055923f23/CVE/Clinic's%20Patient%20Management%20System/SQLi/2.png)

![image](https://github.com/CyberThoth/CVE/blob/5198ef2d56f9c818654bbe131c7f7e3055923f23/CVE/Clinic's%20Patient%20Management%20System/SQLi/3.png)

