```bash
dnf install mock
usermod -a -G mock <user>

mock -r fedora-37-x86_64 --init
mock -r fedora-37-x86_64 --install lorax-lmc-novirt vim-minimal pykickstart

sudo setenforce 0

mock -r fedora-37-x86_64 --shell --old-chroot --enable-network

livemedia-creator --ks flat-fedora-live-WKS.ks --no-virt --resultdir /var/lmc --project Fedora-WKS-Live --make-iso --volid Fedora-WKS-37 --iso-only --iso-name Fedora-SoaS-27-x86_64.iso --releasever 37 
```

