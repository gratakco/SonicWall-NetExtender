# Download SonicWall NetExtender

Download the latest release from [Releases](https://github.com/linkfold/SonicWall-NetExtender/releases/tag/10.3.0)

## Introduction

**NetExtender** is the official SSL-VPN client developed by SonicWall for Windows, designed to offer encrypted remote access to private networks via a secure SSL tunnel. It enables users to connect to internal resources from nearly any location, ensuring a reliable and protected remote work setup.

This repository is an unofficial guide aimed at enhancing the experience of using NetExtender on Windows. It’s crafted to simplify installation, improve connection stability, and support automation for advanced users. Whether you're a typical user or a systems administrator, this guide will assist in resolving issues, establishing reliable connections, and automating VPN tasks using practical utilities and scripts.

Please note: This repository does not include the NetExtender installer or any proprietary components. It strictly serves as a companion guide for maximizing the use of the official NetExtender application on Windows systems.

## Compatible Platforms

### **Windows**

* **Windows 10 and 11 (64-bit)**
* Administrator rights are necessary for setup
* Can be operated through both graphical UI and the command-line tool

> While SSL VPN web portals might offer browser-triggered downloads, NetExtender runs independently as a client and doesn't operate inside the browser environment.

### **Linux (Limited Support)**

* Legacy compatibility includes **Ubuntu 18.04**, **Red Hat-based systems**, and **OpenSUSE**
* Available in `.tgz` and `.rpm` formats
* Known compatibility issues with newer Linux kernels (5.x and above)
* Lacks integration with `systemd` and modern network frameworks

> SonicWall recommends Linux users migrate to **SMA Connect Tunnel** or use WebVPN through supported browsers. The Linux NetExtender client is deprecated and may fail to function on modern systems.

### **SonicWall Device Compatibility:**

NetExtender works seamlessly with the **SonicWall SMA series** and **firewalls running SonicOS version 6.5 or higher**.

## Installing NetExtender

The installation wizard will guide you through the process. It’s generally best to stick with the default installation directory unless custom paths are needed. During installation, Windows might prompt warnings about drivers or certificates—these messages can safely be approved.

After installation, launch NetExtender from either the Start Menu or the system tray. The client supports both GUI and CLI modes and may auto-start depending on system policies.

Before making your first connection, ensure your firewall or antivirus solution isn't interfering with NetExtender’s traffic. On corporate networks, specific certificates or additional settings may be necessary to establish a successful connection.

Although a reboot is typically unnecessary, restarting the machine can help resolve initial connection issues after installation.

Once setup is complete, you're ready to configure your VPN profile and begin using NetExtender securely.

## Key Features

NetExtender delivers a native SSL VPN experience for Windows, designed to work hand-in-hand with SonicWall’s Unified Threat Management (UTM) and Next-Gen Firewall platforms. Unlike IPSec-based VPNs, it utilizes SSL/TLS protocols to provide full network-level access over HTTPS (TCP port 443), making it highly effective in restrictive environments.

One of NetExtender's standout capabilities is its **Layer 3 tunneling**, which offers full IP communication between remote clients and internal systems without relying on split tunneling or complex NAT schemes. It supports both IPv4 and IPv6, and dynamically retrieves routing and DNS data from the server.

Authentication is also a strong point—it supports **directory services** such as LDAP, RADIUS, and various multi-factor solutions, making it a solid choice for corporate environments with centralized identity management. Detailed session logs deliver rich diagnostic information for audit and support purposes.

The client includes dual interfaces: graphical and command-line. Its CLI enables complete automation, including scripted VPN connections and task scheduling, which is especially useful on headless or service-based systems.

On the security front, NetExtender supports TLS encryption (1.2+), optional mutual certificate validation, and—where configured—Endpoint Control Policies (EPC). It installs a lightweight virtual interface and forms a secure tunnel with minimal system load or user disruption.

For IT personnel managing distributed or hybrid infrastructures, NetExtender’s out-of-the-box compatibility with NAT environments, proxies, and captive portals ensures consistent connectivity, especially useful for mobile teams or decentralized workforces.

## Setting Up NetExtender

### VPN Profile Creation

You can define and save multiple connection profiles for easy access to different VPN gateways.

1. Open **NetExtender** and go to the **Connection Profiles** section.
2. Click **Add New Profile**.
3. Fill in the required connection parameters:

   * **Server Address:** `vpn.yourcompany.com`
   * **User credentials**
   * **Domain (if needed)**
4. Press **Save** to store the profile.

> \[!info] **Tip:**
> Enabling **auto-connect** can accelerate future logins.

   * **Automatic detection via WPAD**
   * **Manual entry** (specify proxy server and port)

## How to Use NetExtender

### Initiating a VPN Connection

1. Launch the **NetExtender** client.
2. Either pick a saved profile or manually enter your connection details:
