# Home Lab and Infrastructure Documentation

For a while now, I've been slowly adding to a home server project as a way to familiarize myself with Linux, take greater ownership and resposibility for my data, and also, I just think it's really cool.

My server's name is Rhubarb, a play on words that refers to the Raspberry Pi it's hosted on (rhubarb pie is also delicious), but also a bit a nod to the concept of "rhubarb forcing", a method of growing rhubarb where it's grown in a hot, dark environment that leads it to grow much faster than normal, and creates sweeter, more tender stalks. With Rhubarb (the server), I'm employing chaos engineering to acheive a similar goal: when put under high loads (stress testing), the system must learn (via automation) how to survive (stay up) and grow, leading to a much more resilient and desirable outcome (a server with built-in, automated failsafes).

![A diagram of my home server, showing my Raspberry connected to the Gateway with Ethernet, and exposing 5 services publicly. There's also a Wireguard port, which exposes 4 other services to devices in the VPN network](photos/my_network.png)

### About This Repo

This repo has two main components:

**`/rhubarb`**
- Configuration files that are crucial for the operation of the server (Docker, WireGuard, CoreDNS)
- Automation scripts that are responsible for detecting and recovering from fail states

**`/herbicide`**
- Files for Terraform and Ansible configuration
- Chaos testing scripts that are run from Ansible

