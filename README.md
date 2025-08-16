# 🖥️ Angel's Homelab

---

## 🔐 How I Setup WireGuard VPN

Using **PiVPN** and **FreeDNS**.

Before any of this could work, I needed to configure my **router**:
- Reserved my server’s IP address (Static DHCP).
- Added a port forwarding rule for **UDP 51820** (WireGuard’s default port).

### Steps:
1. Created a subdomain:  
   **`angulikescomputers.mooo.com`** via FreeDNS.  
   (FreeDNS makes dynamic DNS possible so I can connect from anywhere.)

2. Installed PiVPN (which automates WireGuard setup):  
   ```bash
   curl -L https://install.pivpn.io | bash
   ```

3. During setup:  
   - User: myself (single-user system).  
   - VPN: **WireGuard** over OpenVPN.  
   - Port: kept default (51820).  
   - DNS provider: **CloudFlare**.  
   - DNS entry: my subdomain (`angulikescomputers.mooo.com`).  

4. After setup:  
   - Added a client profile:  
     ```bash
     pivpn add
     ```  
     (I named mine `Ubuntu`.)

   - Generated a QR code:  
     ```bash
     pivpn -qr
     ```  
     (Scanned into the WireGuard mobile app.)

5. ✅ Now I can connect into my system from anywhere securely.

### What I Learned:
- How to configure and deploy a VPN for secure access.  
- Router networking (static DHCP, port forwarding).  
- Documentation & tracking processes.  
- Encryption & Access Control basics.  
- Network troubleshooting (inside vs. outside network).  

---

## 📂 How I Setup Samba (File Sharing)  
_On the way…_

---

## 🌐 How I Setup DNS  
_On the way…_

---

## ⚙️ How I Setup Automation  
_On the way…_

---
