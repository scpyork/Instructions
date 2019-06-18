### Avoid.
#### (If you can avoid it, it saves a lot of hastle)


1. You must disable safeboot from the bios
2. You then install the drivers from the displaylink-debian repo on github
3. Update the xorg configuration file - and remove any others in the dir. 
`sudo gedit /etc/X11/xorg.conf.d/20-displaylink.conf`
And insert:
```
Section "Device"
    Identifier  "DisplayLink"
    Option      "PageFlip" "false"
    Option      "TearFree" "true"

EndSection

```
