# ⚠️ DOM XSS – jQuery Selector Sink via `hashchange` Event (PortSwigger Labs)

---

## 🧠 Lab Title:
**DOM XSS in jQuery selector sink using a `hashchange` event**

---

## 🎯 Lab Objective:
Exploit a DOM-based XSS vulnerability where jQuery uses untrusted data from `location.hash` (triggered via `hashchange` event) inside a selector, allowing attacker-controlled DOM manipulation.

---

## 🧪 Root Cause:

The JavaScript behaves like this:
```javascript
$(window).on('hashchange', function(){
    var el = $(location.hash);
    el.text('You clicked a link!');
});
