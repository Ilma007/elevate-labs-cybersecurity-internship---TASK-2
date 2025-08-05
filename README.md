# elevate-labs-cybersecurity-internship---TASK-2
analyze a phishing email 
TASK 2 – PHISHING EMAIL ANALYSIS REPORT

Objective:
The objective of this task is to analyze a suspicious email sample and identify characteristics that indicate potential phishing activity.

Tools Used:

Email client / saved .eml file

Free online EML analyzer

VirusTotal – for checking if the sender IP/domain is flagged as malicious

1. Email Metadata and Routing Details

Message ID: <20230919183549.39DEA3F725@ubuntu-s-1vcpu-1gb-35gb-intel-sfo3-06>

From Address: BANCO.BRADESCO@ATENDIMENTO.COM.BR (spoofed domain; does not match legitimate Bradesco email infrastructure)

Sender IP Address: 137.184.34.4 (associated with DigitalOcean VPS – not an official bank mail server)

Date (UTC): 2023-09-19 18:35:49

2. Authentication and Security Checks

SPF: temperror – Sender Policy Framework check failed due to DNS lookup error.

DKIM: none – No digital signature found to verify authenticity.

DMARC: temperror – Domain-based Message Authentication, Reporting & Conformance not applied due to DNS error.

CompAuth: FAIL – Microsoft authentication result indicates message originated from an unauthenticated source.

3. Spam and Threat Indicators

SpamAssassin Score: 0.30 (low numeric score but still contains phishing indicators)

Flagged Issues:

Email contains only HTML content (no plain text alternative).

Unbalanced HTML <body> tags – indicative of automated or malicious email generation.

URLs linked to suspicious external domains.

Spamhaus DBL query blocked; one domain listed as malicious:

blog1seguimentmydomaine2bra.me (high-risk phishing domain)

4. Content and Language Analysis

Subject Line: "CLIENTE PRIME - BRADESCO LIVELO: Seu cartão tem 92.990 pontos LIVELO expirando hoje!"

Urgency tactic used (“expiring today”) to pressure the recipient into immediate action.

Language: Portuguese

Message Style: HTML email with branded styling, Google Fonts, and embedded images.

Call-to-Action: “Resgatar Agora” (Redeem Now) – directs user to malicious phishing domain.

5. Embedded Links and Domains

Displayed Link: https://blog1seguimentmydomaine2bra.me/ (not affiliated with Bradesco; likely used for credential theft)

Domain Characteristics: Recently registered, contains brand reference mixed with random words, lacks legitimacy.

6. Technical Red Flags

Originates from a VPS hosting provider rather than a corporate mail server.

Base64 encoding used for message body – a common obfuscation technique in phishing.

No valid email authentication records present in the header.

7. Indicators of Compromise (IOC)

IP Address: 137.184.34.4

VirusTotal Result: Flagged as malicious by multiple security vendors.

Domain: blog1seguimentmydomaine2bra.me

VirusTotal Result: Recently registered, flagged as phishing/malicious.

8. Final Verdict
⚠ PHISHING EMAIL – HIGH RISK
The email demonstrates multiple phishing characteristics, including:

Spoofed sender domain

Failed authentication checks

Urgent call-to-action

Malicious external link

9. Recommendations

Do not click any embedded links.

Report the email to the IT or Security department.

Block the sender IP and associated domain at the network firewall level.

Conduct awareness training for users to recognize similar phishing attempts.

Use VirusTotal or similar tools to verify suspicious IPs and domains before taking further action.

10. Conclusion
This analysis confirms that the examined email is a sophisticated phishing attempt leveraging:

Brand impersonation

Social engineering tactics

Technical obfuscation

Immediate action, including reporting, blocking malicious domains, and enhancing user awareness, is essential to mitigate potential data breaches and financial loss.
