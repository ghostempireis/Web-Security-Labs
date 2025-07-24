# 🔥 Reflected XSS into Attribute (Angle Brackets HTML-Encoded)

## 🧪 Lab Details
- **Lab Name**: Reflected XSS into attribute with angle brackets HTML-encoded
- **Platform**: PortSwigger Web Security Academy
- **Lab Type**: Cross-Site Scripting (XSS)
- **Difficulty**: 🟢 Apprentice
- **Date**: 24 July 2025
- **Status**: ✅ Completed

---

## 🎯 Objective
Exploit a reflected XSS vulnerability by injecting JavaScript inside an **HTML attribute** where angle brackets are encoded but **quotes are not**.

---

## Tool Used 
Burp Suite Repeater – to modify and test requests
Firefox Browser – to trigger and verify alert popups
PortSwigger Labs – vulnerable environment



## 🚀 Payload Used

```html
" onmouseover="alert(1)
