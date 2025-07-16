# ✅ DOM XSS via `document.write(location.search)`

**🧪 Lab**: PortSwigger - DOM XSS in `document.write` sink using `location.search`  
**🔐 Level**: Apprentice  
**📅 Date Solved**: 2025-07-16  
**💼 Author**: Ranjan Kumar

---

## 🧠 Vulnerability Overview

This lab demonstrates a DOM-based Cross-Site Scripting (XSS) vulnerability caused by unsafe use of `document.write()` with unsanitized user input from `location.search`.

---

## 🔍 Code Snippet (Vulnerable)

```javascript
var query = location.search;
document.write(query);
