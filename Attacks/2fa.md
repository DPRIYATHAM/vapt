# 2FA - 2 Factor Authentication

Two-factor authentication (2FA) is a security method that requires two forms of identification to access an account or resource. It's also known as two-step verification or dual-factor authentication. 

3 Types of keys:
1. Possession - Card, Keys...
2. Knowledge - Passwords
3. Inheritence - Biometrics

- 2FA systems generally use Password+OTP 
- OTP Bruteforce is a severe vulnerability, where attacker tries for reset password and brute-forces the OTP required to reset.
    - Intruder in Burpsuite can do this task easily to automate this process.
    - Successful attack could make the victim loose access to the account.
    - Mitigations could be rate limiting the requests.
