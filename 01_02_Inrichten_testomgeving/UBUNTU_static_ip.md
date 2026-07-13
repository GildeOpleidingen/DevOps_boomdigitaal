# Ubuntu configuration static IP for netwerk interface

Configure your Ubuntu VM in VMWare so that the network card is in the LAN Segment.

Look how your network card is called in Ubuntu:
```bash
ip a
```
You need this name in the configuration.

You need to addfollowing into a yaml file:
(watch indentation!)

```bash
sudo nano /etc/netplan/01-netcfg.yaml
```

File content:
Change the ens33 to your network interface name (see ip a)
Change the routes to your gateway (VyOS internal interface)

```yaml
network:
  version: 2
  ethernets:
     ens33:
       dhcp4: false
       addresses:
         - 10.0.0.20/24
       nameservers:
         addresses:
           - 10.0.0.5
       routes:
         - to: default
           via: 10.0.0.5  

```

Change rights of this file with:

```bash
sudo chmod 600 /etc/netplan/01-netcfg.yaml
```

Activate configuration:

```bash
sudo netplan apply
```