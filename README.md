# UniFi OS 3.x WPA Supplicant for AT&amp;T Fiber

Since the new update to UniFi OS 3.x, Ubiquti has removed support for podman, which some may have been relying on for wpa_supplicant to bypass the AT&amp;T Fiber Residential Gateway. There are ways to launch an equivalent container with [nspawn-container](https://github.com/unifi-utilities/unifios-utilities/tree/main/nspawn-container), but I haven't been able to get it to work with nspawn. In any case, here's a file to run it directly on UniFi OS and make it persistent!


Trying to keep it simple as possible. Enjoy!


## Semi-Automated Steps
1.	Get certs (I assume you have this already if you’re looking to make this work for UniFi OS 3.x)
2.	Download this package/folder (wpa_supplicant).
3.	Copy certs to wpa_supplicant folder package
    - Rename as:
      - CA.pem
      - Client.pem
      - PrivateKey.pem
4.	Update the MAC Address of your certs in wpa_supplicant.config.
5.	Enable SSH on UDM/UDM Pro/UDM SE
6.	SSH to UDM/UDM Pro/UDM SE as root user.
7.	SCP wpa_supplicant folder to /data
8. 	`cd /data/wpa_supplicant`
9.	`chmod +x install.sh`
10.	`./install.sh`

## Manual Steps
TBD

## Donations
### [Buy Me a ~~Coffee~~ Beer](https://bmc.link/jphamdev)
