# Some Cytips

This file contains some useful tips, and code snippets, that help in VAPT

1. SQL Injection
Get Database tables: (Helps when you don't table names in the Database)
`UniOn selEct 1,table_name frOm information_schema.tables table_schema = '[database name]' /*`

### Exploitation Methods
1.  Veil Framework - Used for generating payloads - [GitHub](https://github.com/Veil-Framework)<br>
`sudo apt install -y veil`
2. Crunch - used to create a wordlist
`> crunch [min] [max] [characters] -t [pattern] -o [FileName]`
3. Hydra - tool that can be used to bruteforce almost any authentication service.
`> hydra [IP] -L [usernames] -P [passwords] [service]`

