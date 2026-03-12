# Command Injection

## Overview
Command Injection is a vulnerability that occurs when a web application executes system commands using user input without proper validation or sanitization. Attackers can inject additional commands and execute them on the server.

DVWA contains a vulnerable feature that allows testing of command injection attacks.

---

## Objective

- Understand how command injection vulnerabilities occur
- Exploit command execution through user input
- Learn how attackers gain system information through injected commands

---

## Vulnerable Functionality

The DVWA application includes a feature that allows users to ping an IP address.

Example functionality:
ping <user_input>  

If the application directly inserts user input into a system command, attackers can inject additional commands.

---

## Attack Methodology

1. Identify the input field accepting user data.
2. Intercept the request using **Burp Suite** (optional).
3. Inject command separators to execute additional commands.
4. Observe the server response.

---

## Example Payloads

Execute multiple commands:
127.0.0.1; ls  

Check current user:
127.0.0.1 && whoami  

Read sensitive files:
127.0.0.1 | cat /etc/passwd 


---

## Exploitation Result

Successful command injection allows attackers to:

- Execute arbitrary system commands
- Retrieve sensitive system information
- Enumerate directories and files
- Gain deeper access to the server

---

## Impact

- Remote command execution
- Information disclosure
- Server compromise
- Privilege escalation
- Full system takeover

---

## Mitigation

- Validate and sanitize all user inputs
- Avoid executing system commands with user input
- Use secure APIs instead of system calls
- Implement allowlists for permitted inputs
- Apply the principle of least privilege
- Use proper escaping mechanisms

---

## Tools Used

- DVWA (Damn Vulnerable Web Application)
- Kali Linux
- Burp Suite
- Web Browser Developer Tools

---

## References

- OWASP Command Injection
- OWASP Top 10: Injection

