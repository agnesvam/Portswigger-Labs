# PortSwigger Labs

This repository is a personal learning log for PortSwigger Web Security Academy labs with Burp Suite.

The goal is to document not only that a lab was completed, but also the reasoning, the Burp workflow, the exploit path, and the mitigation lesson behind it.

## Learning objective

Build a clear, portfolio-style record of practical web security learning by capturing:

- the vulnerability being tested
- the method used to exploit it
- the impact of the issue
- the fix that should be applied


## Completed labs

### Authentication

- [Username Enumeration via Different Responses](labs/authentication/username-enumeration-via-different-responses/README.md)
- [2FA Simple Bypass](labs/authentication/2fa-simple-bypass/README.md)

### Access control

- [User ID Controlled by Request Parameter, with Unpredictable User IDs](labs/access-control/user-id-controlled-by-request-parameter-unpredictable-user-ids/README.md)
- [User ID Controlled by Request Parameter with Password Disclosure](labs/access-control/user-id-controlled-by-request-parameter-with-password-disclosure/README.md)



## Notes for future labs

- Keep write-ups concise and readable
- Include screenshots of important Burp requests and responses
- Focus on the root cause, not just the exploit
- Add a mitigation section for each lab
- Use consistent naming so the repo stays easy to browse

A starter template is available in [templates/lab-writeup-template.md](templates/lab-writeup-template.md).

## PortSwigger Academy references

- Authentication labs: https://portswigger.net/web-security/authentication
- Access control labs: https://portswigger.net/web-security/access-control
