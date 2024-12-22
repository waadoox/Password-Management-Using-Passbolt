# Passbolt Password Manager Project

This project demonstrates the secure deployment of the Passbolt password manager using AWS, Namecheap, and Let's Encrypt for SSL/TLS encryption.

## Features
- Hosted Passbolt on AWS EC2 instance.
- Registered a custom domain with Namecheap.
- Configured SSL/TLS encryption with Let's Encrypt.
- Set up secure SSH access for server management.

## Access Details
- **Passbolt URL**: [https://cybereditproject.info](https://cybereditproject.info)
- **Public IP**: `13.40.228.225`

## SSL Certificate
- **Certificate Location**: `/etc/letsencrypt/live/cybereditproject.info/fullchain.pem`
- **Key Location**: `/etc/letsencrypt/live/cybereditproject.info/privkey.pem`
- **Expiration**: 2025-03-21
- Automatically renewed using Certbot.

## Configuration Steps
1. Set up an EC2 instance on AWS.
2. Register a domain on Namecheap and point it to the public IP.
3. Install and configure Passbolt:
   - Update `nginx` with your domain in `/etc/nginx/sites-enabled/nginx-passbolt.conf`.
   - Reconfigure Passbolt with `dpkg-reconfigure passbolt-ce-server`.
4. Enable HTTPS:
   - Use Certbot to request and deploy an SSL certificate.
   - Reload `nginx` to apply the changes.
5. Complete the installation at [https://cybereditproject.info](https://cybereditproject.info).

## Security Details
- **SSH Key Fingerprint**:

- **Database Credentials**:
Credentials are stored in `/root/.mysql_credentials` and should be secured appropriately.

## Screenshots
- Passbolt Login Page:
![Login Page](screenshots/passbolt_login.png)
- SSL Configuration:
![SSL Secure](screenshots/ssl_secure.png)

## Future Enhancements
- Implement 2FA for added security.
- Set up monitoring and alerting with AWS CloudWatch.
- Automate database backups.


