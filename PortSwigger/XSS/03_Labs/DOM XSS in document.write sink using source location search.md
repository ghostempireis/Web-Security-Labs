# 🚨 DOM XSS Lab Reports – PortSwigger Web Security Academy

---

## 🧪 Lab 1: DOM XSS in `document.write` Sink using `location.search` Source

### 🔍 Lab Overview

This lab demonstrates a DOM-based Cross-Site Scripting (XSS) vulnerability where untrusted input from the `location.search` source is passed directly into `document.write()` without proper sanitization.

**🎯 Goal:** Trigger a JavaScript alert by exploiting DOM XSS.

---

### 🔎 Vulnerable JavaScript Code

```javascript
document.write(location.search);




