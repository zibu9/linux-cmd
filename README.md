# linux-cmd
all linux cmd memo


## Edit cart 

    ### Ubuntu / Debian

    ```batch
      sudo netplan list
    ```

    or 
    ```batch
      ip a
    ```
Next 
    
    ```batch
      sudo nano /etc/netplan/filename.yaml
      network:
  version: 2
  ethernets:
    enp0s25:  # Replace enp0s25 with your interface name
      dhcp4: no
      addresses: [192.168.1.2/24]
      gateway4: 192.168.1.1
      nameservers:
        addresses: [8.8.8.8, 8.8.4.4]

        sudo netplan apply


    ```
