# ⚠️ DOM XSS – jQuery Anchor Href Attribute Sink using location.search (PortSwigger Labs)

---

## 🧠 Lab Title:
**DOM XSS in jQuery anchor `href` attribute sink using `location.search` source**

---

## 🎯 Lab Objective:
Exploit a DOM-based XSS vulnerability where jQuery sets the `href` attribute of an anchor element using untrusted input from `location.search`.

---

## 🧪 Root Cause:

The vulnerable code behaves like this:
```javascript
$('a#link').attr('href', location.search);
