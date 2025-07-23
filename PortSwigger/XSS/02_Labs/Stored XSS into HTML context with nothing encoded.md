# 💥 Stored XSS into HTML Context with Nothing Encoded

## 🧪 Lab Overview

This lab demonstrates a basic **Stored Cross-Site Scripting (XSS)** vulnerability where user input is stored on the server and rendered into an HTML page **without any encoding**. Our goal is to inject a malicious script that executes when the page is viewed.

> ✅ Objective: Inject a script that executes when a blog post comment is viewed.

---

## 🛠️ Tools Used

- 🧩 **Burp Suite Community Edition**
- 🌐 **Firefox DevTools**
- 💻 **PortSwigger Web Security Academy Lab Instance**

---

## 🕵️‍♂️ Step-by-Step Exploitation

### 1. 🏁 Open the Lab

- Logged into the lab instance provided by PortSwigger.
- Navigated to the **blog post** section where comments can be added.

### 2. 💬 Add a Malicious Comment

- Identified the comment form containing `name`, `email`, and `comment` fields.
- Crafted the following payload in the **Comment** field:

```html
<script>alert('XSS by Ranjan')</script>
