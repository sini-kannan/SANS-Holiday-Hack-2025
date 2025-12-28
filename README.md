SANS Holiday Hack Challenge 2025 – Technical Write-up
This repository contains a technical analysis of my favorite objectives from the SANS Holiday Hack Challenge 2025. As a Master of Science in Cybersecurity student at IMT Atlantique, my focus was on applying formal methodology and logic to solve complex security puzzles.

🚀 Overview
The following objectives were completed by combining browser-based inspection, manual logical deduction, and pattern recognition. These challenges highlight that security is often about understanding Business Logic rather than just finding coding errors.

🛠️ Completed Objectives
1. IDORable Bistro
Objective: Identify the gnome linked to a specific sushi order by analyzing the web application.

Methodology:

Utilized Browser Developer Tools to intercept network requests.

Identified an API endpoint that processed receipt IDs.

Observed that ID values were sequential, indicating a lack of object-level obfuscation.

Performed Manual Parameter Manipulation to access receipts not intended for the current session.

Security Concept: Insecure Direct Object Reference (IDOR). This occurs when an application provides direct access to objects based on user-supplied input without a secondary authorization check.

2. Dosis Network Down
Objective: Perform a root-cause analysis on a failing network service.

Methodology:

Conducted behavioral analysis by observing service responses.

Compared baseline (expected) behavior against actual failing states.

Used Logical Elimination to narrow down points of failure within the connection string.

Security Concept: Network Service Resilience and troubleshooting. This emphasizes the importance of visibility in complex network architectures.

3. Rogue Gnome Identity Provider
Objective: Detect a malicious identity provider (IdP) within an authentication flow.

Methodology:

Deconstructed the Authentication Handshake to see how identity tokens were trusted.

Performed a differential analysis between valid and rogue identity responses.

Identified inconsistencies in the verification process.

Security Concept: Authentication Trust Abuse. This highlights the dangers of misconfigured Federated Identity systems.

4. Quantgnome Leap
Objective: Retrieve a hidden flag by navigating a system through chained SSH keys.

Methodology:

Performed lateral movement by discovering SSH keys in user home directories.

Used discovered credentials to pivot from low-privileged accounts to administrative accounts.

Accessed the protected file system to read the flag.

Security Concept: Privilege Escalation and SSH Key Management. This demonstrates the risk of "Credential Stuffing" or key reuse within an internal environment.

5. Going in Reverse
Objective: Solve a system puzzle by working backward from a known output.

Methodology:

Analyzed the final system state to determine the required input.

Applied Reverse Reasoning to deconstruct the system's logic steps.

Security Concept: Reverse Engineering Logic. Understanding the "Expected Output" is a critical skill for debugging and identifying logic flaws.

🧠 Key Takeaways
Logic over Code: Many critical vulnerabilities stem from flawed business logic, not just syntax errors.

Zero-Trust Client: Client-side browsers should never be trusted with sensitive data or sequential IDs.

Human Persistence: Manual analysis with a web inspector is often more effective than automated tools when dealing with custom logic.

🎓 About the Author
I am a DevSecOps Engineer with 2.5 years of experience at Bank of America. I am currently pursuing an MSc in Cybersecurity and seeking a Final Year Internship starting in June 2026.
