Artbox
================================

![artbox](https://raw2.github.com/danasf/artbox/master/img/artbox-logo.png)

Turn your dated, OpenWRT capable router into a platform for hosting browser-based, interactive web art. 

A tool for activists, artists, protests, public events, location specific installations and more.

Please contribute!

Instructions
------------

1. Install [OpenWRT](https://openwrt.org/)

2. Configure Wireless and IP

3. edit /etc/dnsmasq.conf
```
address=/#/10.10.0.1
```
4. Move LuCI from port 80
edit /etc/config/uhttpd
```
# Artbox
config uhttpd main
    list listen_http    0.0.0.0:80
    option home        /artbox
    option cgi_prefix     /cgi-bin

# LuCI or admin area, if desired
config uhttpd secondary
    list listen_http    0.0.0.0:8080
    option home        /www
    option cgi_prefix     /cgi-bin
```

Todo
------------
* script to auto-config all changes
* example art
* file-manager / WYSIWYG for easy page creation 


Inspiration
------------

* [PirateBox](http://daviddarts.com/piratebox-diy-openwrt/?id=PirateBox_DIY_OpenWrt#Tutorial_A:_TP-Link_MR3020)
* [LibraryBox](http://jasongriffey.net/librarybox/)
