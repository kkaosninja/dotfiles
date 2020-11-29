# Linux Config Files
Repo containing config files for my customized Kubuntu system


***|Description|Links
---|---|---
OS | Kubuntu 20.10 | https://kubuntu.org/
Kernel | Xanmod 5.9 STABLE | https://xanmod.org/
Shell | Zsh + OhMyZsh + Powerlevel10k | https://ohmyz.sh/, https://github.com/romkatv/powerlevel10k
Preferred Font | Meslo Nerd Font | https://github.com/romkatv/powerlevel10k |
KDE Plasma Theme | Sweet KDE | https://store.kde.org/p/1294729 |

---

DNS
Requirements => Filters Malicious sites + Support DNSSEC + Support DNS over TLS

Using Quad9 + CleanBrowsing

Reason -> https://www.skadligkod.se/general-security/phishing/malicious-site-filters-on-dns-in-2020/

Other Useful Links:

https://quad9.net/faq/#Does_Quad9_implement_DNSSEC  
https://quad9.net/faq/#Does_Quad9_support_DNS_over_TLS  
https://quad9.net/doh-quad9-dns-servers/ (for DoH support)  
https://cleanbrowsing.org/filters#security  
https://cleanbrowsing.org/guides/dnsovertls  
https://cleanbrowsing.org/guides/dnsoverhttps ( for DoH support)  

Chose DoT resolvers as systemd-resolved only supports DoT  

Links I used to help configure systemd-resolved and NetworkManager:  
https://wiki.archlinux.org/index.php/Systemd-resolved  
https://andrea.corbellini.name/2020/04/28/ubuntu-global-dns/  


**DNSSEC turned off due to multiple issues systemd-resolved seems to be having with DNSSEC, even in `allow-downgrade` mode**  

Faced the "failed-auxiliary" DNSSEC validation error when installing Rust. Also saw considerable slowdown in the `apt update` command.

For more info  
1) https://github.com/systemd/systemd/issues/9867
2) https://fedoraproject.org/wiki/Changes/systemd-resolved#DNSSEC  

---

KDE Plasma Widgets+Addons:
- [Netspeed Widget](https://store.kde.org/p/998895)
- [Simple System Monitor](https://store.kde.org/p/1173509)
- [Thermal Monitor](https://store.kde.org/p/998915)
- [Safe Eyes](https://slgobinath.github.io/SafeEyes/)
