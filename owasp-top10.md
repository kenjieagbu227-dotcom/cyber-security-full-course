
**Purpose:** understand the most critical web app security risks.

Common items (examples):
- **A1: Injection (SQLi)** — attacker injects malicious queries.
- **A2: Broken Authentication** — weak session management.
- **A3: Cross-Site Scripting (XSS)** — inject client-side scripts.
- **A4: Insecure Direct Object References (IDOR)** — unauthorized access to object IDs.
- **A5: Cross-Site Request Forgery (CSRF)** — trick authenticated users to perform actions.

**Practice:** read OWASP Top 10 list and test vulnerable web apps like DVWA or Juice Shop in a lab.


---

🔹 10.2 Burp Suite / OWASP ZAP Usage


**Purpose:** intercept and manipulate web traffic, find vulnerabilities.

**Burp Suite basic flow:**
1. Set browser proxy → Burp intercepts requests.  
2. Use Repeater for manual testing.  
3. Scanner (Pro) for automated checks.

**OWASP ZAP:** open-source alternative with active scan and spidering.

**Quick tip:** configure your browser to use Burp/ZAP as proxy, then browse the target to capture requests.


---

🔹 10.3 Secure Coding Basics (Input Validation & Sanitization)


**Purpose:** prevent vulnerabilities by writing safe code.

**Key practices:**
- **Input validation:** validate server-side (never trust client-side).
- **Output encoding:** escape data before rendering to prevent XSS.
- **Parameterized queries / prepared statements:** prevent SQL injection.
- **Proper authentication & session management.**

**Example (prepared statement in Python):**
```python
cursor.execute("SELECT * FROM users WHERE id = %s", (user_id,))

---


 🔗 Lesson 10.4: API Security Testing

**Purpose:** secure REST/GraphQL APIs and test for common issues.

**Focus areas:**
- Authentication & authorization (JWT, OAuth).
- Rate limiting and input validation.
- Sensitive data exposure in responses.
- Broken object-level authorization (IDOR).

**Tools:** Postman, Burp, OWASP ZAP, API-specific scanners.

**Example test:** try accessing another user's data by changing the ID in the API call (check for proper authorization).


 
🌐 Lesson 10: Web Application Security

### Subtopics:
1. [OWASP Top 10](lesson10-1-owasp-top10.md)  
2. [Burp Suite & OWASP ZAP](lesson10-2-burp-suite-and-owasp-zap.md)  
3. [Secure Coding Basics](lesson10-3-secure-coding-basics.md)  
4. [API Security Testing](lesson10-4-api-security-testing.md)
