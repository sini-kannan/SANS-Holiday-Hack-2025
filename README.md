SANS Holiday Hack Challenge 2025 – Technical Write-up

This repository contains a short technical write-up of my favourite objectives from the SANS Holiday Hack Challenge 2025.
The focus is on how each problem was approached and which security concepts were involved.

Completed Objectives

IDORable Bistro

Dosis Network Down

Rogue Gnome Identity Provider

Quantgnome Leap

Going in Reverse

1. IDORable Bistro
Objective

Find the gnome linked to a sushi order by analyzing a web application.

Approach

Opened browser developer tools

Inspected network requests made by the page

Found an API endpoint that accepted a receipt ID

Noticed that the ID values were sequential numbers

Changed the ID manually to access other receipts

Result

One receipt contained sushi-related information, which revealed the correct gnome name.

Security Concept

Insecure Direct Object Reference (IDOR) caused by missing access control on backend objects.

2. Dosis Network Down
Objective

Identify why a network service was not working correctly.

Approach

Observed how the service responded to requests

Compared expected behavior with actual behavior

Looked for missing or broken connections

Used logical elimination instead of automated tools

Result

The cause of the network issue was identified and the objective was completed.

Security Concept

Basic network troubleshooting and service analysis.

3. Rogue Gnome Identity Provider
Objective

Identify a malicious identity provider affecting authentication.

Approach

Reviewed the authentication flow

Analyzed how identity information was trusted

Compared valid and invalid identity responses

Noticed inconsistencies in identity verification

Result

The rogue identity provider was identified.

Security Concept

Authentication trust abuse and identity misconfiguration.

4. Quantgnome Leap
Objective

Gain access to a system using chained SSH keys and retrieve a flag.

Approach

Logged into multiple user accounts using SSH keys

Found keys stored in user home directories

Used each key to access the next account

Reached an administrative account

Read the flag file from the system

Result

The flag was retrieved and submitted successfully.

Security Concept

SSH key management and privilege escalation through key reuse.

5. Going in Reverse
Objective

Solve a problem by working backward from the expected output.

Approach

Read the objective description carefully

Focused on what the final answer needed to look like

Reversed the logic step by step

Derived the correct input value

Result

The correct value was submitted and accepted.

Security Concept

Reverse logic and reasoning based on system behavior.

Overall Lessons Learned

Many security issues are logic problems, not coding errors

Client-side behavior should never be trusted with sensitive data

Browser developer tools are powerful for security testing

Manual analysis is often required when tools show nothing

Reading carefully is as important as using tools
