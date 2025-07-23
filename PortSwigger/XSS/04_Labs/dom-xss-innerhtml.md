# ⚠️ DOM XSS – innerHTML Sink using location.search (PortSwigger Labs)

---

## 🧠 Lab Title:
**DOM XSS in `innerHTML` sink using source `location.search`**

---

## 🎯 Lab Objective:
Exploit a DOM-based XSS vulnerability by injecting a malicious payload through the `search` parameter that gets reflected via `innerHTML`.

---

## 🧪 Root Cause:

The page reads untrusted input from `location.search` and directly assigns it to a DOM element using `.innerHTML`:

```javascript
element.innerHTML = location.search;
