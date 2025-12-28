# SANS Holiday Hack Challenge 2025 – Technical Write-up

This repository contains a short technical write-up of my favorite objectives from the **SANS Holiday Hack Challenge 2025**.

The focus is on how each problem was approached and which security concepts were involved.

---

## 1. IDORable Bistro

### Objective
Identify the gnome linked to a sushi order by analyzing a web application.

### Methodology
- Used browser developer tools  
- Inspected network requests  
- Identified an API endpoint handling receipt IDs  
- Observed that ID values were sequential  
- Manually modified IDs to access other receipts  

### Result
A sushi-related receipt revealed the correct gnome name.

### Security Concept
Insecure Direct Object Reference (IDOR) caused by missing access control on backend objects.

---

## 2. Dosis Network Down

### Objective
Perform root-cause analysis on a failing network service.

### Methodology
- Observed service responses  
- Compared expected and actual behavior  
- Looked for broken or missing connections  
- Used logical elimination instead of automated tools  

### Result
The cause of the network failure was identified.

### Security Concept
Basic network troubleshooting and service analysis.

---

## 3. Rogue Gnome Identity Provider

### Objective
Identify a malicious identity provider affecting authentication.

### Methodology
- Reviewed authentication flows  
- Analyzed how identity data was trusted  
- Compared valid and invalid identity responses  
- Identified inconsistencies in verification  

### Result
The rogue identity provider was identified.

### Security Concept
Authentication trust abuse and identity misconfiguration.

---

## 4. Quantgnome Leap

### Objective
Gain system access using chained SSH keys and retrieve a flag.

### Methodology
- Logged into multiple user accounts using SSH keys  
- Found keys stored in user home directories  
- Used each key to access the next account  
- Reached an administrative account  
- Read the flag file from the system  

### Result
The flag was retrieved successfully.

### Security Concept
SSH key misuse and privilege escalation through key reuse.

---

## 5. Going in Reverse

### Objective
Solve a challenge by working backward from the expected output.

### Methodology
- Read the objective carefully  
- Focused on the required final output  
- Reversed the logic step by step  
- Derived the correct input value  

### Result
The correct value was accepted.

### Security Concept
Reverse logic and reasoning based on system behavior.

---

## Overall Lessons Learned

- Many security issues are logic problems, not coding errors  
- Client-side behavior should not be trusted with sensitive data  
- Browser developer tools are very useful for testing  
- Manual analysis is needed when tools show nothing  
- Careful reading matters as much as technical skill  
