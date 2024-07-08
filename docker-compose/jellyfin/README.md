# Jellyfin

## Setup

- Requirements:

  - PCI device mount from host for GPU
  - Install graphics card drivers

    ```bash
    sudo ubuntu-drivers list --gpgpu

    sudo ubuntu-drivers install


    # check installation
    cat /proc/driver/nvidia/version

    nvidia-smi
    ```

- NFS share

  ```bash
  sudo apt update

  sudo apt install nfs-kernel-server

  sudo apt install nfs-common

  sudo mount NAS_ADDRESS:/volume1/jellyfin/media ./media

  df -h

  # add this line to /etc/fstab to mount in every reboot
  NAS_ADDRESS:/volume1/jellyfin/media      /home/rafael/templates/docker-compose/jellyfin/media    nfs     defaults        0       0
  ```

## TODO

- [ ] Setup proper user to access NFS
