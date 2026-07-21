# User ID Controlled by Request Parameter, with Unpredictable User IDs

- Category: Access Control
- PortSwigger Lab: https://portswigger.net/web-security/access-control/lab-user-id-controlled-by-request-parameter-with-unpredictable-user-ids

## Summary
The lab shows that a user can access another user’s data by changing a user ID in the request.

## Objective
Exploit the IDOR by modifying the user ID parameter.

## Vulnerability
Insecure direct object reference (IDOR).

## Tools
Burp Proxy, Burp Repeater, browser.

## Steps
1. Log in and find the user ID in the application flow.
2. Discover another user’s ID from the page content.
3. Replace the user ID in the request.
4. Access the other user’s data.

## Impact
An attacker can read another user’s private data by tampering with the request.

## Mitigation
Enforce server-side authorization for each object access.

## Notes
Exposed identifiers can become a direct path to unauthorized access.

## Proof of Concept / Evidence
- Another user’s ID found in the application response
- Modified request returned the other user’s data

![Proof of Concept](screenshots/lab1.png)