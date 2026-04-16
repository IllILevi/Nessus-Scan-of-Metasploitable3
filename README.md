# Nessus-Scan-of-Metasploitable3
For this project, I did a basic vulnerability scan of the vulnerable network Metasploitable3 using Tenable Nessus. The goal was to find common web-vulnerabilities and determine actionable solutions to mitigate those vulnerabilities. This has helped me gain a deeper understanding and familiarity with vulnerability scanning tools and how to detect and mitigate known vulnerabilities. 

**Ethics & safety disclaimer:**  
*This project was performed in an isolated lab environment. Do not scan systems without authorization.*


## Methodology
I first started with two virtual machines (VM), the attacker machine, using Kali Linux, and the victim machine, using Metasploitable3. Both VM’s were set to Host-Only Network, with Kali Linux having a second network adapter set to NAT in order to access Nessus. 
For Nessus, I did a basic network scan that scanned all ports for all web vulnerabilities and left everything else as default. 

## Findings Summary
From the Nessus scan, there were many detected vulnerabilities, including 12 critical ones, as can be seen in the screenshot below.  

<img width="1918" height="773" alt="Image" src="https://github.com/user-attachments/assets/b4bac1c8-0c5f-4c38-a128-032522a3cb82" />


The top five vulnerabilities are as follows:

**Vulnerability:** 201408 - Canonical Ubuntu Linux SEoL (14.04.x)  

**Synopsis:** An unsupported version of Canonical Ubuntu Linux is installed on the remote host.  

**Solution:** Upgrade to a version of Canonical Ubuntu Linux that is currently supported.  

&ensp;

**Vulnerability:** 92626 - Drupal Coder Module Deserialization RCE  

**Synopsis:** A PHP application running on the remote web server is affected by a remote code execution vulnerability.    

**Solution:** Upgrade the Coder module to version 7.x-1.3 / 7.x-2.6 or later. Alternatively, remove the entire Coder module directory from any publicly accessible website.    

&ensp;

**Vulnerability:** 81510 - PHP 5.4.x < 5.4.38 Multiple Vulnerabilities (GHOST)  

**Synopsis:** The remote web server uses a version of PHP that is affected by multiple vulnerabilities.  

**Solution:** Upgrade to PHP version 5.4.38 or later.  

&ensp;

**Vulnerability:** 58987 - PHP Unsupported Version Detection  

**Synopsis:** The remote host contains an unsupported version of a web application scripting language.  

**Solution:** Upgrade to a version of PHP that is currently supported.  

&ensp;

**Vulnerability:** 84215 - ProFTPD mod_copy Information Disclosure  

**Synopsis:** The remote host is running a ProFTPD module that is affected by an information disclosure vulnerability.  

**Solution:** Upgrade to ProFTPD 1.3.5a / 1.3.6rc1 or later.  



