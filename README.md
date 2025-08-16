# 🖥️ Angel's Homelab

## System Info (Fastfetch)

```ansi
                             ....             Ubuntu Server
              .',:clooo:  .:looooo:.           -------------
           .;looooooooc  .oooooooooo'          OS: Ubuntu 24.04.3 LTS x86_64
        .;looooool:,''.  :ooooooooooc          Host: HP ENVY x360 m6 Convertible
       ;looool;.         'oooooooooo,          Kernel: Linux 6.8.0-71-generic
         ...                ......  .:oo,      Packages: 852 (dpkg)
  .;clol:,.                        .loooo'     Shell: bash 5.2.21
 :ooooooooo,                        'ooool     Terminal: /dev/pts/1
'ooooooooooo.                        loooo.    CPU: Intel(R) Core(TM) i7-6500U (4) @ 3.10 GHz
'ooooooooool                         coooo.    GPU 1: NVIDIA GeForce 930M [Discrete]
 ,loooooooc.                        .loooo.    GPU 2: Intel HD Graphics 520 @ 1.05 GHz [Integrated]
   .,;;;'.                          ;ooooc     Memory: 595.09 MiB / 7.68 GiB (8%)
       ...                         ,ooool.     Swap: 0 B / 4.00 GiB (0%)
    .cooooc.              ..',,'.  .cooo.      Disk (/): 11.06 GiB / 914.78 GiB (1%) - ext4
       .coooooc,..      coooooooooo.           
         .:ooooooolc:. .ooooooooooo'
           .':loooooo;  ,oooooooooc
               ..';::c'  .;loooo:'
```
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
