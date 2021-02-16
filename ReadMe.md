In this project I followed the given scenario.

You are working as a Security Engineer for X-CORP, supporting the SOC infrastructure. The SOC analysts have noticed some discrepancies with alerting in the Kibana system and the manager has asked the Security Engineering team to investigate. 

Flags have been hidden throughout the system. Your goal is to find find the flags and ultimately find the vulnerabilities in the system.

Scan the network to identify the IP addresses of Target 1.

* nmmp image here

Document all exposed ports and services.

* open port image here


Enumerate the WordPress site.

* word press image here


Use SSH to gain a user shell.

* ssh pic

Flag 1 found by searching HTML page source
* flag1

Flag 2 found by using locate command
* flag 2

Find the MySQL database password.

MySQL database password found by viewing the wp-config.php file in /var/www/html

* mysql image


Use the credentials to log into MySQL and dump WordPress user password hashes.

* password hashes


Crack password hashes with john.

* crack hash image

Flag 3 can be found inside the MySQL Database

* flag 3 image
 

Secure a user shell as the user whose password you cracked.

* ssh steven image


Escalate to root. One flag can be discovered after this step.

* python root image

Flag 4 found in root folder of user Steven.

* Flag 4