# 🐞 Stored XSS in Anchor `href` Attribute

## 🧪 Lab Title
**Stored XSS into anchor href attribute with angle brackets HTML-encoded**  
**Platform**: PortSwigger Web Security Academy

---

## 🔍 Vulnerability Type
**Stored Cross-Site Scripting (XSS)**  
Occurs when untrusted input is embedded inside an anchor tag’s `href` attribute without proper sanitization or validation.

---

## 🧠 Description
The application allows user-controlled input to be stored and rendered inside an anchor (`<a>`) element's `href` attribute. Although angle brackets (`<`, `>`) are HTML-encoded, no filtering or sanitization is applied to the URI scheme (e.g., `javascript:`), allowing for JavaScript execution when the link is clicked.

---
## payload are injected in comment field
<a href="javascript:alert(1)">Click here</a>


## 🛠️ Payload Used

```html
javascript:alert(1)
