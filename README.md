# Password Crackathon

## Overview
This project was part of the CYB101 course, focusing on cracking password hashes using the popular tool **John the Ripper**. The goal of the project was to crack as many passwords as possible from a list of unsalted password hashes obtained from famous breaches such as the 2012 LinkedIn and 2016 Yahoo Data breaches. The purpose of this exercise was to highlight the importance of strong password policies and help users understand the vulnerabilities of weak passwords.

## Project Goals
By completing this project, I was able to:
- Write custom `john` commands
- Use different wordlists and rule sets
- Utilize custom mask-based rules for password cracking
- Communicate the findings through a report

## Cracking Strategy
The task was broken down into several key steps:
1. **Crack at least 250 passwords**: This was the primary objective, and it was accomplished using different strategies outlined below.
2. **Use different wordlists**: One of the first attempts was using the `rockyou.txt` wordlist, which contains commonly used passwords.
3. **Apply built-in rules**: I used John’s built-in rules, like `--rules=jumbo`, to enhance the cracking process by applying additional permutations to the wordlists.
4. **Use a custom mask**: A custom mask like `?l?l?d?d?d?S` was utilized to target passwords with specific patterns, such as two lowercase letters followed by three digits and a special character.

## Example Commands
Below are some example commands I used in this project:

1. **Using a different wordlist**:
    ```bash
    john --wordlist=rockyou.txt CPLeak.txt
    ```

2. **Using a built-in ruleset**:
    ```bash
    john --rules=jumbo --wordlist=rockyou.txt CPLeak.txt
    ```

3. **Using a custom mask**:
    ```bash
    john --mask=?l?l?d?d?d?S --wordlist=rockyou.txt CPLeak.txt
    ```

## Results
By running the commands mentioned above, I successfully cracked over 250 password hashes. Here’s a summary of the results:
- **Total Passwords Cracked**: 250+ passwords
- **Wordlists Used**: `rockyou.txt`, `lower.lst`
- **Built-in Rules Applied**: `jumbo`
- **Custom Masks Used**: Targeted lowercase letters, digits, and special characters
