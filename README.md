# Linux Config Files
Repo containing config files for my customized Pop OS system


***|Description|Links
---|---|---
OS | Pop OS 20.04 LTS | https://pop.system76.com/
Kernel | Xanmod 5.8 STABLE | https://xanmod.org/
Terminal Emulator | Alacritty | https://github.com/alacritty/alacritty
Shell | Zsh + OhMyZsh + Powerlevel10k | https://ohmyz.sh/, https://github.com/romkatv/powerlevel10k
Preferred Font | JetBrains Mono | https://github.com/JetBrains/JetBrainsMono/releases |


**NOTE:** After installation of custom kernel, the symlinks of initrd.old and vmlinuz.old point to the new kernel and initrd and vmlinuz point to the generic kernel. Don't forget to change this. Also dont forget to copy kernel images to /boot/efi/EFI/Pop_OS-{UUID} of both current and previous kernels.

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

GNOME Extensions:
https://extensions.gnome.org/extension/779/clipboard-indicator/  
https://extensions.gnome.org/extension/945/cpu-power-manager/  
https://extensions.gnome.org/extension/36/lock-keys/  
https://extensions.gnome.org/extension/1320/nvidia-gpu-stats-tool/  
https://extensions.gnome.org/extension/53/pomodoro/  
https://extensions.gnome.org/extension/906/sound-output-device-chooser/  
https://extensions.gnome.org/extension/1460/vitals/  

---

Graphics Drivers:  
Pop OS Default NVIDIA Driver version 440.1 does not work with Kernel 5.8.  
So installing latest 450 series drivers from NVIDIA Graphics Drivers team PPA  

`
sudo add-apt-repository ppa:graphics-drivers/ppa -y  
sudo apt update  
sudo apt install nvidia-driver-450 libnvidia-gl-450 libnvidia-gl-450:i386 libvulkan1 libvulkan1:i386 -y  
`

Above lines ripped off from https://christitus.com/ultimate-linux-gaming-guide/#nvidia-proprietary-driver-install
