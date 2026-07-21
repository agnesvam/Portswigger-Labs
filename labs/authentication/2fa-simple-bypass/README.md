# 2FA Simple Bypass

- Category: Authentication
- PortSwigger Lab: https://portswigger.net/web-security/authentication/multi-factor/lab-2fa-simple-bypass

## Summary
The lab shows that 2FA can be bypassed if session handling is weak after the first login step.

## Objective
Bypass the second authentication factor by abusing the session state.

## Vulnerability
2FA bypass through session handling flaws.

## Tools
Burp Proxy, Burp Repeater, browser.

## Steps
1. Log in as a user and complete the first authentication step.
2. Access the account page and note the session behavior.
3. Log out and try to access the account with a different user context.
4. Observe that the session state allows access without properly completing the second factor.

## Impact
An attacker could access another user’s account if the session is not properly invalidated.

## Mitigation
Rotate and invalidate session tokens after login and logout.

## Notes
2FA is not enough if the session handling is flawed.

## Proof of Concept / Evidence
- Session behavior reused across accounts
- Account page accessible after the initial login step



![Proof of Concept](authentication\screenshots\lab1.png)