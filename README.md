# Linux Config Files
Repo containing config files for my customized Pop OS system


***|Description|Links
---|---|---
OS | Pop OS 20.04 LTS | https://pop.system76.com/
Kernel | Xanmod 5.7 STABLE | https://xanmod.org/
Terminal Emulator | Alacritty | https://github.com/alacritty/alacritty
Shell | Zsh + OhMyZsh + Powerlevel10k | https://ohmyz.sh/, https://github.com/romkatv/powerlevel10k


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

Chose DNS over TLS as systemd-resolved only supports DoT


Links I used to help configure systemd-resolved and NetworkManager:

https://wiki.archlinux.org/index.php/Systemd-resolved

https://andrea.corbellini.name/2020/04/28/ubuntu-global-dns/

GNOME Extensions:

https://extensions.gnome.org/extension/779/clipboard-indicator/

https://extensions.gnome.org/extension/945/cpu-power-manager/

https://extensions.gnome.org/extension/36/lock-keys/

https://extensions.gnome.org/extension/1320/nvidia-gpu-stats-tool/

https://extensions.gnome.org/extension/53/pomodoro/

https://extensions.gnome.org/extension/906/sound-output-device-chooser/

https://extensions.gnome.org/extension/1460/vitals/
