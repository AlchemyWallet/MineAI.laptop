Output from Nanominer when powerLimit set:

```Could not set clocks for device 0 because of insufficient permissions.
To enable setting device clocks, in Ubuntu 18.04 do the following:
sudo gedit /usr/share/X11/xorg.conf.d/10-nvidia.conf
Edit the "Coolbits" option to 31. Then your file should look like this:
Section "OutputClass"
    Identifier "nvidia"
    MatchDriver "nvidia-drm"
    Driver "nvidia"
    Option "AllowEmptyInitialConfiguration"
    Option "Coolbits" "31"
    ModulePath "/usr/lib/x86_64-linux-gnu/xorg"
EndSection
Finally reboot.
```
