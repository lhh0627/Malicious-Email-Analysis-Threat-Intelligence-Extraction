# Malicious-Email-Analysis
The goal of this simulated lab was to investigate a credential-harvesting phishing campaign, analyze the malicious email headers to trace the attacker's origin, and extract indicators of compromise (IOCs) without detonating the payload.



---

<details>
<summary><b>📖 Background: The Anatomy of Email & Phishing (Click to expand)</b></summary>

Every phishing email you’ll investigate starts with something simple: an email address. If you don’t understand how it’s structured, you may overlook the very clues attackers rely on. Email as we know it today was popularized in the 1970s on ARPANET by Ray Tomlinson, who introduced the @ symbol to separate the user from the destination system.

### Anatomy of an Email Address
An email is composed of the following elements:
1. **Username:** Identifies the specific recipient’s mailbox on the email server.
2. **@ symbol:** Separates the username from the domain and tells the system where to route the email.
3. **Domain name:** Specifies the mail server responsible for receiving the message.

> **Analogy:** Think of an email address as a home mailing address. The **domain** is like the street or apartment building, and the **username** is the specific person within that location. With both pieces of information, the mail server knows exactly where to deliver the message.

### Core Email Protocols
When you send an email, several protocols work together behind the scenes:
*   **SMTP (Simple Mail Transfer Protocol):** Sends emails outward.
*   **POP3 (Post Office Protocol):** Downloads emails to a single device. Emails are typically removed from the server after download.
*   **IMAP (Internet Message Access Protocol):** Syncs emails across multiple devices. Emails remain on the server unless explicitly deleted.

### An Email's Journey
Rather than memorizing definitions, here is the path an email takes from sender to receiver:
1. **User sends an email:** The sender’s email client sends the message to their mail server using SMTP.
2. **Mail server queries DNS:** The sending server asks DNS for the recipient domain’s mail server.
3. **DNS responds:** DNS returns the address of the recipient’s mail server.
4. **Email is delivered:** The message is sent across the Internet to the recipient’s server.
5. **The recipient checks their mailbox:** The recipient’s email client connects to their mail server.
6. **Email is retrieved:** The message is downloaded (POP3) or synced (IMAP) to the recipient’s device.

</details>

---
