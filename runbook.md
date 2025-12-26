# Runbook

This runbook has three major sections:
1. Setup, getting from 0 to where I'm currently at
2. Maintenance, how to modify and extend functionality
3. Troubleshooting, ways I've found to diagnose and solve issues efficiently

This is quite a long document, so I advise you *Ctrl+F* for your desired section and/or keyword.

# Setup
*Going from 0 to Rhubarb*

This section's divided into 3 subsections, focusing on setting up initial access, adding security, and finally adding some convenient network features.

1. Initial Access
	1. OS
	2. SSH
2. Security
	1. Wireguard
	2. UFW
3. Conveniences
	1. CoreDNS
	2. Borg
	3. Samba
# Maintenance
*How to configure and extend the existing feature set*

Here, I'll go over how to perform regular system actions, focusing largely on extending functionality (adding new services, sites, timers).

1. Adding a new service with Docker
2. Proxying to a new network service (i.e. a docker service) with Nginx
3. Proxying to website files with Nginx
4. Adding a new Wireguard peer
# Troubleshooting
*Ways I've found to efficiently diagnose and solve issue*
