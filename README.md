# Password Management System Using Passbolt

## Overview
This project demonstrates the deployment and configuration of a secure password management system using **Passbolt**, hosted on an **AWS EC2 instance**. The project integrates a custom domain registered via **cybereditproject.info** and implements secure access protocols to adhere to cybersecurity best practices.

## Key Features
- Hosted Passbolt instance on AWS cloud platform.
- Custom domain configuration using Namecheap.
- Secure access using **SSL/TLS** and **SSH**.
- Adherence to network security principles and protocols.

---

## Technologies Used
- **AWS**: EC2 instance for hosting Passbolt.
- **Namecheap**: Domain registration and configuration.
- **Ubuntu**: Operating system for configuring SSL and managing the server.
- **Passbolt**: Open-source password management tool.
- **Protocols**: TCP/IP, SSL/TLS, SSH for secure data transmission.

---

## Project Architecture
1. **AWS EC2 Instance**: 
   - Public IP: `13.40.228.225`.
   - Instance configured to host Passbolt.
2. **Namecheap Domain**:
   - Domain linked to AWS server.
3. **SSL Configuration**:
   - Ensures encrypted communication using Let's Encrypt.
4. **Secure Access**:
   - SSH for managing the server.
   - SSL/TLS for encrypted client-server communication.

---

## Setup and Configuration

### 1. Setting Up the AWS Instance
- Launch an EC2 instance on AWS.
- Choose Ubuntu as the operating system.
- Configure security groups to allow SSH, HTTP, and HTTPS access.

### 2. Domain Configuration with Namecheap
- Register a domain on [Namecheap](https://www.namecheap.com).
- Update the DNS settings to point the domain to the AWS EC2 instance's public IP (`13.40.228.225`).

### 3. Secure Access with SSH
- Generate an SSH key pair.
- Use the private key to securely connect to the EC2 instance:
  ```bash
  ssh -i "your-key.pem" ubuntu@13.40.228.225
