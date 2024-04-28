# Vulnerability Assessment and Penetration Testing
This documentation contains the approach and steps needed for VAPT.

### Lab Setup
Linux Distribution => Kali Linux (Debian) - [Download](https://cdimage.kali.org/kali-2024.1/kali-linux-2024.1-installer-amd64.iso)<br>
Hypervisior => VMware Workstation 17 Player - [Download](https://customerconnect.vmware.com/en/downloads/details?downloadGroup=WKST-PLAYER-1751&productId=1377&rPId=117008)<br>
Using Metasploitable for testing purpose - [Download](https://docs.rapid7.com/metasploit/metasploitable-2) <br>


**Rule 1:** Always use a Virtual Machine to do VAPT.<br>
Reason for using VM:
1. Isolation from Host OS 
2. Easy to configure, and test accross different versions
3. Easy to work on networks, saving state.

![Kali VM](assets/kalivm.png)

### Aim
Gain the Control over Application & Database
> If you can't gain control over application, gain control over the programs in the computer (server), exploit computer. <br>
> If nothing works, exploit humans(admins, maintainers) social engineering attacks, side-channel attacks.

### Information Gathering

**Rule 2:** More Information => More Attack Surface <br>

1. Use `Robtex DNS` lookup under “names pointing to same IP”.
2. Using `bing.com`, search for ip:"target ip".
3. `Knock` can be used to find subdomains of target
    1. Download it > git clone https://github.com/guelfoweb/knock.git
    2. Navigate to knock.py. > ce knock/knock.py
    3. Run it > python knock.py [target]
4. Find files & directories in target website tool => dirb `> dirb [target] [wordlist] [options]`
5. Maltego is an information gathering tool that can be used to collect information about ANYTHING. `maltegoce`
6. Domain tools - IP information about our Target website => [whois.domaintools.com](https://whois.domaintools.com/) & [Robotex](https://www.robtex.com/)
7. Netcraft - information regarding IP, Tech Stack, Deployment, Geolocation details => [Netcraft](https://sitereport.netcraft.com/)

### Preparation
1. Login to metasploitable2 > msfadmin/msfadmin
2. `ifconfig` > Get the IP address of the Metasploitable
3. Setup Kali Linux => The attack machine
`
### Vulnerabilities

**Rule 3:** DIE (Discover - Intercept - Exploit)

#### OWASP TOP 10 Web Application Security Risks
![alt text](assets/owasp10.png)

Other Web Vulnerabilities - [Link](https://drive.google.com/file/d/1T_kTLNWVA2uhPcZaVSVrbr2CveY8M3Hp/view)

### Some Useful Links:
1. OWASP Cheatsheet - [Documentation](https://cheatsheetseries.owasp.org/index.html)
2. Metasploitable is an 'intentionally vulnerable virtual machine' by Rapid7 - [Documentation](https://docs.rapid7.com/metasploit/quick-start-guide)
3. Detailed Linux Commands Explaination - [Explainshell](https://explainshell.com)
4. DAMN VULNERABLE WEB APPLICATION (DVWA) - [GitHub](https://github.com/digininja/DVWA)
5. VAPT Documentation by [Revanth](https://github.com/K-REVANTH) - [Document](https://docs.google.com/document/d/12U0AGqMa1BVCar6eaP-_AgwEXOc4ZQS8X7w1Qu2BDmw)