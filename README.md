# Website Redirect Malware Investigation (Simulated Incident)

This project is based on a **simulated cybersecurity incident** scenario from the Google Cybersecurity Professional Certificate. The purpose of the project is to analyze a website compromise that resulted in users being redirected to a malicious domain after downloading an infected executable.

---

## 📌 Scenario Overview

Customers reported to the helpdesk for the website **yummyrecipesforme.com** that they were being prompted to download a file in order to access free recipe content. After executing the downloaded file, users observed:

- Their computer performance slowing down
- The website being redirected to **greatrecipesforme.com**
- Unexpected browser behavior

This indicated that the website may have been **compromised** and distributing **malicious content**.

---

## 🔍 Investigation Summary

Based on the simulated network activity from the course materials, the following sequence of events occurred:

1. The browser sent a **DNS request** to resolve `yummyrecipesforme.com`.
2. The DNS server returned the correct IP.
3. The browser sent an **HTTP request** to load the page.
4. The webpage triggered the download of a **malicious executable**.
5. After the executable was run, the browser performed another **DNS request** for `greatrecipesforme.com`.
6. The browser then sent an **HTTP request** to the attacker-controlled website.
7. A senior analyst confirmed that **malicious JavaScript** had been injected into the original site.

---

## 🧠 Root Cause

The legitimate website `yummyrecipesforme.com` had been **compromised**.  
Attackers injected **malicious JavaScript** that:

- Prompted visitors to download an executable
- Redirected users’ browsers to the malicious domain `greatrecipesforme.com`

---

## 🚨 Impact

- Users may unknowingly execute malware
- System performance degradation
- Possible unauthorized access or further infection
- Loss of trust in the website

---

## ✅ Recommended Remediation

To limit similar attacks in the future:

- Remove the malicious JavaScript from the site
- Patch and secure the web server
- Implement **web application monitoring** (e.g., file integrity checks)
- Educate users to avoid downloading unknown executables

### Additional Recommendation (Brute Force Prevention)

Implement an **Account Lockout Policy**:

| Setting | Recommended Value |
|--------|-------------------|
| Failed login attempts allowed | 5 |
| Lockout duration | 15 minutes |
| Reset counter after | 15 minutes |

This slows or prevents brute-force password attacks.

---

## 📝 Disclaimer

This project is based on a **simulated security incident** from the Google Cybersecurity Professional Certificate.  
No real user data, logs, or malware samples are included.

---

## 🎯 Skills Demonstrated

- Incident documentation
- Understanding of DNS and HTTP traffic flow
- Malware delivery chain analysis
- Security report writing
- Remediation recommendation development

---

## 👤 Author

Anaswara Raj
Aspiring Cybersecurity Analyst  
