# Vulnerability Report: Reflected Cross-Site Scripting (XSS)

## 1. Executive Summary
A **Reflected Cross-Site Scripting (XSS)** vulnerability was identified on the **Altoro Mutual** web application (`http://demo.testfire.net`) via the `[Insert Parameter Name, e.g., query]` parameter on `[Insert Page Path, e.g., /search.jsp]`. User-supplied input is reflected directly in the HTTP response without proper validation or output encoding, allowing arbitrary JavaScript execution in the victim's browser.

- **Target Application:** Altoro Mutual (`http://demo.testfire.net`)
- **Affected Endpoint:** `[Insert Full URL, e.g., http://demo.testfire.net/search.jsp]`
- **Vulnerable Parameter:** `[Insert Parameter Name, e.g., query]`
- **Vulnerability Category:** Reflected Cross-Site Scripting (CWE-79)
- **Severity:** Medium (`CVSS:3.1/AV:N/AC:L/PR:N/UI:R/S:C/C:L/I:L/A:N` — Score: 6.1)

---

## 2. Technical Description
Reflected XSS occurs when an application receives untrusted user input in an HTTP request and immediately returns that data in the response HTML without proper sanitization or context-aware output encoding. An attacker can craft a malicious URL containing JavaScript code and trick a user into clicking it, causing the script to execute within the victim's browser session.

---

## 3. Steps to Reproduce
1. Open the target page: `[Insert Page URL, e.g., http://demo.testfire.net/index.jsp]`.
2. Locate the `[Insert Input Field / Parameter, e.g., Search bar / query parameter]`.
3. Inject the following Proof-of-Concept (PoC) payload:
   ```html
   <script>alert(document.domain)</script>
