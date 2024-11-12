# Fix resolve.conf when setting up systemd networking on Arch Linux

Tuesday, 12 November 2024. 15:39:16GMT

When installing a program in a newly-installed Arch Linux system, `yay` in this case, I noticed that all the go
packages could not be found. The urls were not resolving.

I use `systemd-networkd` and `systemd-resolved`

Turns out that you need to symlink the resolve.conf that comes with systemd:

```bash
sudo ln -sf /run/systemd/resolve/stub-resolv.conf /etc/resolv.conf
```

