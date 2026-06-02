# 🚀 HTTP JavaScript Injector

[![Python Version](https://img.shields.io/badge/python-3.6%2B-blue)](https://www.python.org/downloads/)
[![License](https://img.shields.io/badge/license-MIT-red)](LICENSE)
[![Educational](https://img.shields.io/badge/purpose-educational-yellow)]()

A powerful educational tool for understanding HTTP packet manipulation and JavaScript injection in network traffic.

## ⚠️ Disclaimer

> **This tool is for EDUCATIONAL PURPOSES only!**
> 
> Only use this on networks you own or have explicit permission to test. 
> Unauthorized packet injection or interception may violate laws and regulations.

## 🎯 Features

- 🔍 Intercept HTTP packets in real-time
- ✂️ Remove `Accept-Encoding` headers for readable content
- 💉 Inject custom JavaScript code into HTML responses
- 📊 Automatically update `Content-Length` headers
- 🎨 Colored console output for better visibility

## 📋 Prerequisites

- Python 3.6 or higher
- Linux OS (Kali Linux, Ubuntu, etc.)
- Root privileges
- iptables

## 🛠️ Installation

### Clone the repository
```bash
git clone https://github.com/YOUR_USERNAME/http-injector.git
cd http-injector
```
## 🚀 Usage
Start ARP spoofing (if targeting another device):

```bash
echo 1 > /proc/sys/net/ipv4/ip_forward
arpspoof -i eth0 -t TARGET_IP GATEWAY_IP
```
Run the injector:
```bash
sudo python3 http_injector.py
Stop with Ctrl+C (automatically cleans iptables)
```

## 📖 How It Works
Packet Interception: Uses netfilterqueue and iptables to capture HTTP packets

Request Modification: Removes Accept-Encoding to prevent compression

Response Injection: Adds JavaScript code before </body> tag

Header Update: Recalculates and updates Content-Length
