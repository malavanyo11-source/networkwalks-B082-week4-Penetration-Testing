Web Application Penetration Test — Mediroza General Hospital
Confidential Security Assessment — Authorized Educational Engagement

Table of Contents
Click any section to jump directly to it:
Executive Summary
Scope & Methodology
Tools Used
Attack Surface Discovery
Findings
Milestone Results
Risk Rating Summary
Overall Risk Assessment
Recommendations & Remediation
Evidence Handling & Privacy
Lessons Learned
Image Evidence
Disclaimer

Executive Summary
This report documents the Week 4 penetration testing engagement performed on the Mediroza General Hospital patient portal. The assessment focused on authentication mechanisms, server behavior, and potential exposure of sensitive information. Multiple weaknesses were identified, including username enumeration and predictable error responses.

Scope & Methodology
The assessment followed a black‑box methodology. Only publicly accessible components of the Mediroza Hospital web application were tested. No privileged credentials were used.

Testing included:
Reconnaissance
Endpoint discovery
Authentication testing
Input manipulation
Response analysis
Manual and automated attack simulation

Tools Used
Burp Suite Community Edition
WhatWeb
WAFW00F

Attack Surface Discovery
Initial reconnaissance identified the following key components:

Public homepage
Patient portal login page
Staff login page
Lab reports section (authenticated)
Multiple PHP endpoints

Findings
Finding 1 — Username Enumeration
The login page reveals whether a username exists by returning different error messages. This allows attackers to confirm valid accounts.

Finding 2 — Predictable Error Responses
Incorrect passwords return a different message than unknown usernames, enabling brute‑force profiling.

Finding 3 — Intercepted Login Request
Burp Suite interception shows sensitive request headers and parameters.

Finding 4 — Intruder Attack Simulation
Automated payload testing shows consistent response lengths, indicating no rate‑limiting or lockout mechanisms.

Milestone Results
Reconnaissance complete
Authentication testing complete
Intruder attack simulation complete
Response analysis complete

Overall Risk Assessment
The Mediroza Hospital patient portal is at critical risk due to authentication weaknesses that can be exploited for account discovery and brute‑force attacks.

Recommendations & Remediation
Implement generic error messages
Add rate‑limiting and lockout mechanisms
Enforce CAPTCHA on login
Monitor failed login attempts
Harden server configuration

Evidence Handling & Privacy
All evidence was collected ethically under authorized educational scope. No real patient data was accessed or stored.

Lessons Learned
This assessment demonstrates how small authentication weaknesses can escalate into major security risks. Proper error handling and rate‑limiting are essential.

Disclaimer
This penetration test was performed strictly for educational purposes under authorized scope. No unauthorized access or misuse occurred.
