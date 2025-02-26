# XML External Entity - XXE

![alt text](assets/xxe.png)

#### 3 Types of XML Entities
1. Internal 
2. External
3. Paramater
![alt text](assets/typexxe.png)
![alt text](assets/typexxe2.png)

- Blind XXE
    - The attacker cannot directly see the response but can infer information based on the server's response time or error messages.
- In-Band XXE
    - The attacker sends an XML request and receives a response containing the requested data, allowing them to retrieve sensitive information.
- Out-of-Band XXE 
    - The attacker uses the XXE vulnerability to exfiltrate data to a remote server they control, bypassing traditional security.


### Mitigations
1. Disable External Entities
2. Input Validation and Sanitization
3. Limit XML Parsing Permissions

## Payloads  - https://github.com/swisskyrepo/PayloadsAllTheThings
### Encode - https://urlencoder.org

### LFI - Local File Inclusion
![alt text](assets/lfi.png)

### Mitigations - defusedxml package
![alt text](assets/defused.png)

`content-type: application/xml`

### Hands-on
![alt text](assets/xxehands.png)