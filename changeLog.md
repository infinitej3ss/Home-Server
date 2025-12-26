# Change Log

The following contains formatted diary-like entries of each days worth of work on the server. I began working on it a good while before I began this documentation, so a few of the features (wireguard, samba, minecraft server) will not be discussed here. For information on those, take a look at **runbook.md**.

### Before December 21st, 2025

Changes:
- Build a server for 4 months and then reset it because you downloaded the wrong OS-type
- Flash 64-bit Debian OS onto Raspberry Pi 5
- Configure SSH
- Start Minecraft server

To tell a brief story of the server that came before, around August of this year, I began working on a home server, inspired by a friend who already had one. I was also getting into front-end and wanted to have my own website, but was quite put off by the model of paying a company to serve files for you when you could "just as easily" (not really true) do it yourself.

I had also begun using Linux earlier in the summer, so it was sort of no-brainer to keep the tinkery, do-it-myself kind of mindset going when it came to hosting my website. It also seemed like a whole different beast compared to hosting a desktop. I was super interested in the new set of capabilities available when you had a host that was always on.

This first server started as a basic web server with nginx as a reverse proxy to website files, but I began pushing my boundaries *bit by bit* (haha) with automating backups with rsync, using Wireguard to create a virtual private network, and using docker images to extend services in a clean, predictable, self-contained fashion.

However, my undoing was that, well, I basically started this project as a total novice, and in my ignorance I had installed the 32-bit Raspbian OS instead of the 64-bit version. If you're not quite sure what this means, basically, I installed an OS that used 32-bit addresses instead of 64-bit, which, while my 64-bit CPU could support this (just ignore the extra bits!), it greatly reduced the capability of the server.

The most blatant example is that, since memory addresses are used to *address* (name, refer to) bytes of memory, with 32-bits, you can only *address* 2^32 bytes = 4,294,967,296 bytes = 4GB of memory. This is a limitation of a family of CPUs that never needed to worry about more than 4GB of memory, so they weren't constructed to be able to work with any more.

As my server was getting more complex, and I was wanting to add more services, I also noticed a major lack of support for 32-bit software, and realized I the switch to 64-bit was inevitable. The semester had been extremely intense, so I didn't have time to do it then, but as soon as winter break started, I got to started.

Since every executable is compiled for the CPUs specific kind of architecture, my old 32-bit binaries would be inefficient at best, and broken at worst. It was easier to just copy over the things I wanted to keep and wipe everything else.

It was quite fun doing the basic setup again. I flashed the OS using on a MicroSD with `dd`, set up wifi with `wpa_supplicant.conf`, and configured SSH to include my laptop's public key in `authorized_keys` so I could access it securely.

After this, I set up a Minecraft server for my friends so we could play over winter break together. This was a really fun start to getting back into my server, as it clearly had an immediate, positive impact, and was quite simple to do.

To get back to where I was before I changed 0Ses, I still needed to setup my VPN (Wireguard) and my docker containers for my media servers (Jellyfin, Navidrome). With that, you're all caught up.
 
### December 21st, 2025

Changes:
- Configure Wireguard

### December 22nd, 2025


### December 23rd, 2025


### December 24th, 2025