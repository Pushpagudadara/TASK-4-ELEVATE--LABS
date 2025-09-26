# TASK-4-ELEVATE--LAB

# 🔐 Cyber Security Internship – Task 4  

## 📌 Setup and Use a Firewall on Windows/Linux  

### 🎯 Objective  
Configure and test basic firewall rules to allow or block traffic using **UFW (Linux)** or **Windows Firewall**.  

---

## 🛠️ Tools Used  
- **Linux UFW (Uncomplicated Firewall)**  
- Terminal (for commands)  
- Windows Firewall (alternative)  

---

## ⚙️ Steps Performed  

### 1. Check firewall status  
```bash
sudo ufw status

2. Enable firewall (if inactive)

sudo ufw enable

3. List current rules

sudo ufw status numbered

4. Block inbound traffic on Telnet (Port 23)

sudo ufw deny 23

5. Test rule

Tried telnet localhost 23 → connection blocked ✅


6. Allow SSH (Port 22)

sudo ufw allow 22

7. Restore original state (remove Telnet block)

sudo ufw delete deny 23


---

📸 Screenshots

(Add screenshots here as proof of execution)

screenshots/status.png – UFW status

screenshots/block_port23.png – Port 23 blocked

screenshots/allow_ssh.png – Port 22 allowed



---

📖 Explanation

A firewall filters network traffic based on rules (allow/deny).

Port 23 (Telnet) was blocked because it is insecure (no encryption).

Port 22 (SSH) was allowed to ensure secure remote access.

After testing, rules were reset to original state.



---

✅ Interview Question Notes

1. What is a firewall?
A firewall is a network security tool that filters incoming and outgoing traffic based on rules.


2. Difference between stateful and stateless firewall?

Stateful: Tracks connection state and makes intelligent decisions.

Stateless: Examines each packet independently.



3. What are inbound and outbound rules?

Inbound: Control traffic entering the system.

Outbound: Control traffic leaving the system.



4. How does UFW simplify firewall management?
It provides simple commands (allow, deny) instead of complex iptables rules.


5. Why block port 23 (Telnet)?
Because Telnet is insecure (plain-text, vulnerable to sniffing).


6. What are common firewall mistakes?

Leaving unnecessary ports open

Forgetting to allow SSH/RDP access (locking yourself out)

Misconfigured rules



7. How does a firewall improve network security?
It reduces attack surface and prevents unauthorized access.


8. What is NAT in firewalls?
Network Address Translation hides internal IPs by mapping them to public.


--
