# Echelon Coach API HTTPS Recovery

A public technical case study documenting production HTTPS recovery work for the Echelon Coach virtual wellness training platform.

**Live platform:** [echeloncoach.com/virtualpt](https://echeloncoach.com/virtualpt/)

![Echelon Coach virtual wellness training storefront](assets/echelon-coach-virtualpt-storefront.png)

## Context

Echelon Coach provides live one-to-one virtual fitness and wellness training. The customer-facing experience depends on a secure API connection for critical application functionality.

## Problem

An expired TLS certificate disrupted the secure HTTPS path used by the application API. The recovery required diagnosis at the server and reverse-proxy layers, followed by certificate replacement and verification.

## Solution

The recovery work included:

- Diagnosing the HTTPS and reverse-proxy configuration on AWS-hosted Linux infrastructure
- Installing Certbot and the Nginx integration
- Issuing a new Let’s Encrypt certificate for the application endpoint
- Applying the certificate through the active Nginx configuration
- Reloading Nginx after configuration validation
- Confirming a valid HTTPS response after recovery
- Verifying automated certificate renewal through the operating system service

## Result

The secure API connection was restored and a repeatable certificate-renewal path was confirmed. The work connected infrastructure recovery, reverse-proxy configuration, TLS validation, and customer-facing application availability.

## Technology

- AWS
- Linux / Ubuntu
- Nginx
- SSL/TLS
- Let’s Encrypt
- Certbot
- Systemd
- SSH

## Engineering Notes

This public case study intentionally focuses on the recovery pattern and technical outcome. It excludes infrastructure identifiers, access material, network details, and environment-specific configuration values.

---

Developed and documented by **Nícolas Cartín Reyes**.
