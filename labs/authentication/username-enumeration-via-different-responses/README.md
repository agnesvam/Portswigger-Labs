# Username Enumeration via Different Responses

- Category: Authentication
- PortSwigger Lab: https://portswigger.net/web-security/authentication/password-based/lab-username-enumeration-via-different-responses

## Summary
The lab shows that the login form leaks whether a username exists by returning different responses.

## Objective
Find a valid username by comparing responses during login attempts.

## Vulnerability
Username enumeration via different responses.

## Tools
Burp Proxy, Burp Intruder, Burp Repeater.

## Steps
1. Try login with invalid credentials.
2. Compare the response for different usernames.
3. Use Burp Intruder with a username wordlist.
4. Identify the response that differs from the others.
5. Confirm the valid username and use it for password brute-force.

## Impact
An attacker can identify valid accounts and use them for password spraying or credential stuffing.

## Mitigation
Return the same response for valid and invalid usernames.

## Notes
Small response differences can reveal sensitive information.

## Proof of Concept / Evidence
- Longer or different response for the valid username
- Burp Intruder results showing the candidate username
- Username confirmed as `applications`


![Proof of Concept](screenshots/lab2.png)