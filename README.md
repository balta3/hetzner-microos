# hetzner-microos
Script collection for using openSUSE MicroOS on hetzner servers.

## Installation of openSUSE MicroOS

This installation procedure was tested on various AX line servers and on virtual servers on the hetzner cloud

1. Boot the server in the rescue mode and connect using SSH
2. Download the initialisation script:
```
wget https://raw.githubusercontent.com/balta3/hetzner-microos/main/initMicroOSSetup
```
3. Make the script executable:
```
chmod +x initMicroOSSetup
```
4. Run the script
```
./initMicroOSSetup
```

### Configuration using environment variables

Variable     | Default value | Description
------------ | ------------- | -------------
`DISK0` / `DISK1` | _autodetected, like_ `/dev/nvme0n1` | Normally the disks to use are autodetected, you can specify them manually by setting these variables.
`GUI` | `SSH` | Define the protocol to access Yast for the setup process: `SSH` or `VNC`
`DOWNLOAD_BASE` | `http://download.opensuse.org/tumbleweed/repo/oss/boot/x86_64/loader/` | Define the base path for downloading the setup image of openSUSE
`SWAPSIZE` | 32G | Size of the swap partition to create
`ROOTSIZE` | 40G | Size of the root partition to create
