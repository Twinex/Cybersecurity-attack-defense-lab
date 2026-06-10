# Lab Setup Guide

## Objective

Build a safe and isolated penetration testing lab using VirtualBox.

## Requirements

### Hardware

- 16GB RAM (Recommended)
- Quad-Core CPU
- 100GB Free Storage

### Software

- VirtualBox
- Kali Linux
- Metasploitable 2
- Metasploitable 3
- DVWA

---

## Installation

### Step 1: Install VirtualBox

Download and install VirtualBox.

### Step 2: Import Kali Linux

Configure:

- 4GB RAM
- 2 CPUs
- NAT Network

### Step 3: Import Metasploitable 2

Configure:

- 2GB RAM
- Host-Only Adapter

### Step 4: Import Metasploitable 3

Configure:

- 4GB RAM
- Host-Only Adapter

### Step 5: Deploy DVWA

Install:

- Apache
- MySQL
- PHP

Clone DVWA repository and configure database.

---

## Network Configuration

```text
Kali Linux       192.168.56.100
Metasploitable2  192.168.56.101
Metasploitable3  192.168.56.102
DVWA             192.168.56.103
```

## Validation

Verify connectivity:

```bash
ping 192.168.56.101
```

Run an Nmap scan:

```bash
nmap -sV 192.168.56.101
```

The lab is now ready for testing.
