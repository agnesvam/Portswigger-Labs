# User ID Controlled by Request Parameter with Password Disclosure

- Category: Access Control
- PortSwigger Lab: https://portswigger.net/web-security/access-control/lab-user-id-controlled-by-request-parameter-with-password-disclosure

## Summary
The lab shows how changing a user ID parameter can expose another user’s password.

## Objective
Exploit the IDOR to retrieve sensitive account information.

## Vulnerability
Insecure direct object reference (IDOR) with password disclosure.

## Tools
Burp Proxy, Burp Repeater, browser.

## Steps
1. Log in as a normal user.
2. Change the user ID parameter to the target account.
3. Observe the response containing the hidden password.
4. Use the password to log in as the target user.

## Impact
An attacker can take over another user’s account and perform privileged actions.

## Mitigation
Do not expose sensitive data through object references and enforce strict server-side authorization.

## Notes
Access control flaws can leak credentials as well as data.

## Proof of Concept / Evidence
- Retrieved the administrator password from the account page after modifying the user ID parameter.
- Used the discovered password to log in as `administrator`.
- Deleted the user `carlos` to complete the lab.

![Proof of Concept](access-control\screenshots\lab2.png)

