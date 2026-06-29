<img width="4032" height="3024" alt="IMG_0793" src="https://github.com/user-attachments/assets/6644c17f-85a1-4b6d-9528-2cd413b85687" /># home-server
This is my home server creation journey, turning an unused piece of hardware into a server which can run multiple VMs, file-hosting service like Nextcloud, media/audio server like Jellyfin, and lots of cool projects that come to my mind.

# Bare Metal Proxmox Homelab Server Setup

## Overview

This project documents the transformation of a spare desktop computer into a remotely managed bare-metal virtualization server using Proxmox VE.

The goal of this project was to create a personal infrastructure platform capable of hosting future IT administration, cybersecurity, and networking labs while maintaining remote accessibility without requiring physical access to the machine.

---

# Project Goals

- Convert a physical desktop machine into a dedicated virtualization host
- Learn enterprise-style virtualization concepts
- Create a foundation for future Active Directory, cybersecurity, and networking labs
- Enable secure remote administration
- Build practical infrastructure management experience

---

# Hardware Specifications

| Component | Specification |
|---|---|
| CPU | AMD Ryzen 3 3200G |
| RAM | 16GB DDR4 |
| Storage | 256GB SSD + 250GB HDD |
| Operating System | Proxmox VE |
| Access Method | Remote management through Tailscale |

---

# Architecture
Remote Laptop
|
|
Tailscale VPN
|
|
Proxmox VE Server
|
|
Virtual Machines
|
|
Future IT / Cybersecurity Labs


---

# Why Proxmox?

Instead of running virtual machines inside a desktop operating system, Proxmox was installed directly onto the hardware.

This allows the machine to act as a dedicated hypervisor.

Benefits:

- Better resource allocation
- Web-based management
- VM snapshots
- Isolation between environments
- Closer similarity to enterprise virtualization platforms

---

# Installation Process

## 1. Preparing Installation Media

The Proxmox VE ISO was downloaded and written to a bootable USB drive.

Screenshot:

<img width="4032" height="3024" alt="IMG_0793" src="https://github.com/user-attachments/assets/cab3d5f2-5238-4a36-bec8-13509edcb68e" />


---

## 2. Installing Proxmox VE

The machine was booted from the installation media and Proxmox VE was installed directly onto the SSD.

This replaced the previous Linux desktop operating system.

Screenshot:

<img width="2425" height="1364" alt="IMG_0797" src="https://github.com/user-attachments/assets/0cda723c-7bee-476d-8c77-5d03efabbfaa" />


---

## 3. Network Configuration

During installation, network parameters were configured:

- Hostname
- IP address
- Gateway
- DNS settings

Screenshot:

<img width="4032" height="2268" alt="IMG_0796" src="https://github.com/user-attachments/assets/d5c6238c-b315-44ee-9fe1-e9a7da7b5c63" />


---

## 4. First Boot

After installation, the machine booted directly into the Proxmox environment.

Screenshot:

<img width="4032" height="2268" alt="IMG_0798" src="https://github.com/user-attachments/assets/b3322b88-2c79-48d6-acf5-d8f61af1395c" />


---

# Remote Management Setup

## Tailscale

To avoid router port forwarding and expose the server securely, Tailscale was configured.

This creates a private encrypted network between trusted devices.

Architecture:
MacBook
|
|
Encrypted Tailscale Tunnel
|
|
Proxmox Server


Benefits:

- Secure remote access
- No public exposure
- Works across different networks
- Suitable for remote lab management

---

# Skills Practiced

## Virtualization

- Hypervisor installation
- Bare metal deployment
- VM infrastructure planning

## Linux / Server Administration

- Network configuration
- Remote access
- Service management

## Networking

- IP addressing
- VPN connectivity
- Secure remote administration

---

# Future Lab Expansion

This server will be used to host:

- Windows Server Active Directory labs
- Windows client environments
- Linux security tools
- Monitoring systems
- Cybersecurity practice environments

---

# Challenges Encountered

## Challenge 1: Remote Management

Problem:

The machine needed to operate without monitor and peripherals.

Solution:

Implemented remote access using Tailscale.

---

## Challenge 2: Limited Hardware Resources

The system is designed around resource efficiency.

Future virtual machines will be deployed according to available CPU, RAM, and storage capacity.

---

# Key Learnings

Through this project I learned:

- How bare-metal virtualization differs from desktop virtualization
- How hypervisors manage hardware resources
- How secure remote administration works
- How infrastructure is designed before deploying workloads

---

Further projects on this server will be added to files in the repo.
