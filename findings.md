# Some Interesting Findings in the Journey

This file contains some useful tips, and code snippets, findings that help in VAPT

1. SQL Injection
Get Database tables: (Helps when you don't table names in the Database)<br>
`UniOn selEct 1,table_name frOm information_schema.tables table_schema = '[database name]' /*`

Case: ***Code Review >>> Pentest***<br>
Simple cryptography algorithm to sign a user in from site A to site B automatically. <br>
If user is logged into site A -generate_key-> MD5 Hash { username:date }<br>
When a user is passed to site B, he/she will send the key on the query to site B in an HTTP re-direct. <br>
Site B independently computes the hash, and compares it to the hash passed on the request.<br> 
If they match, site B signs the user in as the user they claim to be. <br>
Anyone that figures out the scheme (or is told how it works, or downloads the information from Bugtraq) can log in as any user<br>
Manual inspection, such as a review or code inspection, would have uncovered this security issue quickly. <br>
A black-box would not have uncovered the vulnerability. <br>
It sees a 128-bit hash that changed with each user, and by the nature of hash functions, did not change in any predictable way<br>

### Exploitation Methods
1.  Veil Framework - Used for generating payloads - [GitHub](https://github.com/Veil-Framework)<br>
`sudo apt install -y veil`
2. Crunch - used to create a wordlist
`> crunch [min] [max] [characters] -t [pattern] -o [FileName]`
3. Hydra - tool that can be used to bruteforce almost any authentication service.
`> hydra [IP] -L [usernames] -P [passwords] [service]`

