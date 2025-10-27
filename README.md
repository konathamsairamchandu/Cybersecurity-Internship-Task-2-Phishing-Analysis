# Cybersecurity Internship Task 2: Phishing Analysis

This repository contains the analysis of a real-world phishing email sample as part of my cybersecurity internship.

## Objective
The goal of this task was to obtain a suspicious email, analyze its headers and content, and identify the key indicators of a phishing attack.

## Artifacts
* `BRADESCO LIVELO.eml`: The raw email sample (with headers) used for the analysis.
* `Header-Analysis.pdf`: A PDF report from the MxToolbox email header analyzer, showing the technical breakdown of the email's path and authentication status.
* `ANALYSIS_REPORT.md`: A detailed report (which you are reading now) summarizing the phishing indicators found in the sample.

## Analysis Summary
The email was confirmed as a phishing attack impersonating "Bradesco Livelo." The primary goal is credential harvesting.

### Key Phishing Indicators Found:
1.  **Social Engineering:** Uses extreme urgency ("expiring today") to provoke a panicked reaction.
2.  **Sender Spoofing:** The `From:` address (`atendimento.com.br`) is not the legitimate bank domain.
3.  **Failed Authentication:** The email failed critical security checks, including **DKIM** (it wasn't signed) and Microsoft's **Composite Authentication** (`compauth=fail`).
4.  **Suspicious Origin:** The email was sent from a generic cloud server (`ubuntu-s-1vcpu...`) and not a corporate mail server.
5.  **Malicious Link:** The "Redeem Now" button pointed to a suspicious domain (`...mydomaine2bra.me`) unrelated to the bank.
6.  **High Spam Score:** The email was automatically flagged as Spam (SCL 5) and had a high Bulk Complaint Level (BCL 9).
