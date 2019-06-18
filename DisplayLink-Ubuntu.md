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

    Option      "DRI" "3"             # DRI2 and DRI1 are alternatives if DRI3 performs performs poorly
    Option      "AccelMethod"  "sna" # default
    #Option      "AccelMethod"  "uxa" # fallback
    Option         "Composite" "Disable"
    Option  "TripleBuffer" "true"

EndSection

```

4. *Remove* all lines not containing PATH from /etc/environment. That is do not have :
```
CLUTTER_PAINT=....
CLUTTER_VBLANK=....
```
5. reboot
