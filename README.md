# CTF Assessment Report

## Overview

This repository contains my assessment report and evidence from a Capture the Flag (CTF) exercise.

The main objective was to enumerate the target, identify possible attack paths, gain access where possible, and capture all available flags.

## Attack Path

The assessment followed this general path:

1. Scanned the target and enumerated open ports and services.
2. Identified the web application on port 80 as the main attack surface.
3. Enumerated the WordPress application and discovered valid usernames.
4. Enumerated the `/vendor` and `/wordpress` paths and captured flags.
5. Identified PHPMailer 5.2.16 and researched a suitable exploit.
6. Exploited PHPMailer to gain initial shell access and capture another flag.
7. Further enumerated the MySQL service.
8. Exploited MySQL using User-Defined Functions (UDFs) to gain root access.
9. Captured the final flag.

## Findings

| ID | Finding | Risk |
|---|---|---|
| F-01 | Flag discovered in `/vendor` | Low |
| F-02 | Flag discovered in `/wordpress` | Low |
| F-03 | Initial access through PHPMailer | High |
| F-04 | Root access through MySQL UDFs | High |

## Flags

Four flags were successfully captured during the assessment:

- **Flag 1:** Discovered through `/vendor`
- **Flag 2:** Captured after exploiting PHPMailer and gaining initial shell access
- **Flag 3:** Discovered through `/wordpress`
- **Flag 4:** Captured after exploiting MySQL and gaining root access

## Tools Used

- Nmap
- WPScan
- Burp Suite
- WordPress
- SSH
- MySQL
- Common password lists
- Linux command-line tools

## Lessons Learned

- Proper enumeration helped identify the most useful attack paths.
- Not every open service is immediately exploitable.
- Failed approaches can help guide the next step.
- Validating findings before exploitation is important.
- Keeping clear notes and evidence makes the assessment easier to document.

## Result

All four flags were successfully captured, completing the main objective of the CTF assessment.