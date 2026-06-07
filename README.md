#  Sunny Server

A self-hosted homelab built from an old Intel i3 laptop with 2GB RAM, running Ubuntu Server and Docker.

Instead of letting unused hardware collect dust, I repurposed it into a personal cloud server capable of hosting file storage, photo backup services, remote access, and automated monitoring.

---

##  Why I Built This

I wanted to reduce my dependency on Google Photos and Google Drive for storing my media and files, while also learning Linux, self-hosting, and home server management.

Rather than paying for additional cloud storage, I decided to create my own private cloud infrastructure using an old laptop lying unused at home.

Today, photos uploaded from my phone are stored on my server through Immich, and I can access my files securely from anywhere using Tailscale.

---

##  Hardware

- Intel Core i3 Laptop
- 2 GB RAM
- 460 GB HDD Storage
- Ubuntu Server (Headless)

---

##  Current Usage

- Personal photo backup via Immich
- Remote file access via File Browser
- Secure access from hostel and internship location
- Automated monitoring through Telegram alerts

---

## Technologies Used

- Ubuntu Server
- Docker
- Docker Compose
- Tailscale
- Telegram Bot API
- Bash Scripts
- Linux Networking

---

##  Services Hosted

### Immich

A self-hosted alternative to Google Photos.

Features:
- Automatic photo backup
- Remote access
- Private photo storage
- Mobile synchronization

### File Browser

A lightweight web-based file manager.

Features:
- File uploads/downloads
- Directory management
- Remote file access

---

## Service Dashboard

A custom homepage is hosted on the server root IP, providing a centralized dashboard for accessing all self-hosted services.

The dashboard intelligently separates service links based on connectivity:

- Local Network Access (LAN)
  - Immich
  - File Browser

- Remote Access (Tailscale)
  - Immich
  - File Browser

This allows services to be accessed seamlessly whether devices are connected to the home network or remotely through the Tailscale mesh VPN.
It also eliminates the need to remember individual service ports, providing a single entry point for the homelab.

---
##  Remote Access

The server is connected through a secure Tailscale mesh network.

This allows:

- Accessing services from hostel or anywhere else
- Secure encrypted communication
- No public port exposure
- Simple device authentication

---

##  Monitoring & Automation

A custom Telegram Bot is used for server monitoring.

Current capabilities:

- System status reporting
- Temperature monitoring
- SSH login notifications
- Alert generation when temperature exceeds safe thresholds

This is particularly useful because the server runs on old hardware that can heat up under sustained load.

---

### Challenges Faced

- Running modern self-hosted services on only 2 GB RAM
- Managing thermal limits of aging laptop hardware
- Optimizing Docker containers for limited resources
- Ensuring secure remote access without exposing ports to the public internet

##  Architecture

```text
Phone/Laptop
       │
       ├── Local Network
       │
       └── Tailscale VPN (Remote Access)
                │
                ▼
          Ubuntu Server
                │
                ▼
        Service Dashboard
                │
        ┌───────┴───────┐
        ▼               ▼
     Immich       File Browser

                │
                ▼
          Telegram Bot
```

##  What I Learned

- Linux server administration
- Docker containerization
- Secure remote networking and device connectivity
- Remote system management
- Self-hosted cloud infrastructure
- Service deployment and monitoring
- Automation using Telegram APIs

---

##  Future Improvements

- SSD upgrade
- Additional RAM
- Automated backups
- Monitoring dashboard
- Personalized Family AI Assistant Hosting
- Reverse proxy setup
- HTTPS certificates

---

##  Screenshots

wait ,, will add later

---

##  Project Status

Active and used as a personal cloud server for daily file storage, photo backup, and remote access.
