# Linux Command Memo

## Edit Cart

### Ubuntu / Debian

To list network configurations:

```bash
sudo netplan list
    or
ip a

Next, edit the network configuration file:

```bash
sudo nano /etc/netplan/filename.yaml


Add the following content to filename.yaml:


```bash
    network:
      version: 2
      ethernets:
        enp0s25:  # Replace enp0s25 with your interface name
          dhcp4: no
          addresses: [192.168.1.2/24]
          gateway4: 192.168.1.1
          nameservers:
            addresses: [8.8.8.8, 8.8.4.4]

apply changes

```bash
sudo netplan apply


