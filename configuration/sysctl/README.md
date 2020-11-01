# Sysctl Settings

The `burmilla.sysctl` cloud-config key can be used to control sysctl parameters. This works in a manner similar to `/etc/sysctl.conf` for other Linux distros.

```
#cloud-config
burmilla:
  sysctl:
    net.ipv4.conf.default.rp_filter: 1
```

You can either add these settings to your `cloud-init.yml`, or use `sudo ros config merge -i somefile.yml` to merge settings into your existing system.