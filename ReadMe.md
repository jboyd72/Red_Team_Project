# Red Team Project Overview

In this project I followed the given scenario.

You are working as a Security Engineer for X-CORP, supporting the SOC infrastructure. The SOC analysts have noticed some discrepancies with alerting in the Kibana system and the manager has asked the Security Engineering team to investigate. 

Flags have been hidden throughout the system. Your goal is to find find the flags and ultimately find the vulnerabilities in the system.

## Scan the network to identify the IP addresses of Target 1.

![Screenshot](https://github.com/jboyd72/Red_Team_Project/blob/main/images/nmap_scan.png)
![Screenshot](https://github.com/jboyd72/Red_Team_Project/blob/main/images/nmap_scan2.png)

## Document all exposed ports and services.

![Screenshot](https://github.com/jboyd72/Red_Team_Project/blob/main/images/Vuln_scan1.png)
![Screenshot](https://github.com/jboyd72/Red_Team_Project/blob/main/images/Vuln_scan2.png)
![Screenshot](https://github.com/jboyd72/Red_Team_Project/blob/main/images/Vuln_scan3.png)

## Enumerate the WordPress site.

![Screenshot](https://github.com/jboyd72/Red_Team_Project/blob/main/images/WordPress_scan.png)
![Screenshot](https://github.com/jboyd72/Red_Team_Project/blob/main/images/WordPress_scan2.png)

## Use SSH to gain a user shell.

![Screenshot](https://github.com/jboyd72/Red_Team_Project/blob/main/images/ssh_michael.png)

- Flag 1 found by searching HTML page source

![Screenshot](https://github.com/jboyd72/Red_Team_Project/blob/main/images/flag1.png)

- Flag 2 found by using locate command

![Screenshot](https://github.com/jboyd72/Red_Team_Project/blob/main/images/findFlag.png)
![Screenshot](https://github.com/jboyd72/Red_Team_Project/blob/main/images/flag2.png)

## Find the MySQL database password.

- MySQL database password found by viewing the wp-config.php file in /var/www/html

![Screenshot](https://github.com/jboyd72/Red_Team_Project/blob/main/images/MySql-info.png)

## Use the credentials to log into MySQL and dump WordPress user password hashes.

![Screenshot](https://github.com/jboyd72/Red_Team_Project/blob/main/images/passwordHash.png)

## Crack password hashes with john.

![Screenshot](https://github.com/jboyd72/Red_Team_Project/blob/main/images/crackedHash.png)

- Flag 3 can be found inside the MySQL Database

![Screenshot](https://github.com/jboyd72/Red_Team_Project/blob/main/images/flag3.png)
 
## Secure a user shell as the user whose password you cracked.

![Screenshot](https://github.com/jboyd72/Red_Team_Project/blob/main/images/ssh_steven.png)

## Escalate to root privileges.

![Screenshot](https://github.com/jboyd72/Red_Team_Project/blob/main/images/python-root.png)

- Flag 4 found in root folder of user Steven.

![Screenshot](https://github.com/jboyd72/Red_Team_Project/blob/main/images/flag4.png)

- After expoliting the vulnerabilities to find all 4 flags, the team presented our findings to the SOC manager for further analysis.
