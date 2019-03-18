# fixes pia script

The [pia-nm.sh script](https://www.privateinternetaccess.com/installer/pia-nm.sh) mentioned in the PIA [ubuntu openVPN page](https://www.privateinternetaccess.com/helpdesk/guides/linux/linux/ubuntu-openvpn-setup) didn't work for me at the time of repo creation.  

It seems the script keeps LZO compression off, when it should be turned on.  
See [this commit](29a311f3d003961493eb42d3c7f267e56a6c1070) on what to fix (it might work if ```comp-lzo``` just isn't defined, since the server is trying to push that conflicting setting).



