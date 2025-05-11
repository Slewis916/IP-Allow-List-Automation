
# Python IP Allow-List Automation Script

## Overview
This project simulates an automation script that updates an IP allow-list file by removing unauthorized IP addresses from a restricted file. Designed as part of the Google Cybersecurity Certificate program, the project demonstrates file handling, list manipulation, loops, and logic for access control processes in Python.

## Problem Statement
In security environments, allow-list files are used to manage which IP addresses are granted access to sensitive systems. Occasionally, IPs must be removed due to policy changes or detected threats. This project automates the removal process.

## Objective
To develop a Python script that:
1. Reads a list of authorized IP addresses from a file.
2. Compares it against a file containing restricted IPs.
3. Removes any restricted IPs from the allow-list.
4. Outputs the cleaned allow-list.

## Algorithm Flow
- Read all IP addresses from the main allow-list file.
- Read all restricted IPs from a second file.
- Loop through the allow-list and remove any matches found in the restricted IP list.
- Write the new allow-list back to a file.

## Step-by-Step Logic
1. Open and read the contents of the `allowlist.txt` file into a list.
2. Open and read the contents of the `restricted_ips.txt` file into another list.
3. Iterate through the `allowlist` and remove any IPs that also exist in `restricted_ips`.
4. Write the updated allow-list back to the `allowlist.txt` file.

## Example Code Snippet
```python
with open('allowlist.txt', 'r') as file:
    allowlist = file.readlines()

with open('restricted_ips.txt', 'r') as file:
    restricted_ips = file.readlines()

new_allowlist = [ip for ip in allowlist if ip not in restricted_ips]

with open('allowlist.txt', 'w') as file:
    file.writelines(new_allowlist)
```

## Key Takeaways
- Simulates a real-world access control maintenance task.
- Reinforces understanding of Python file handling and list operations.
- Introduces basic automation concepts for security operations.

## Author
Created by Jashawna Lewis as part of the Google Cybersecurity Certificate program.
