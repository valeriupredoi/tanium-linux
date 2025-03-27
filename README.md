### Deploy and check Tanium on Ubuntu 24

- get the installer and extract it
- create a separate dir where you put these in:
  - `install.sh`
  - `taniumclient_7.6.4.2106-ubuntu24_amd64.deb`
  - `tanium-init.dat`
- install in `/opt` and configure:
```
sudo dpkg -i taniumclient_7.6.4.2106-ubuntu24_amd64.deb
sudo /opt/Tanium/TaniumClient/TaniumClient config set ServerName valeriu
sudo cp tanium-init.dat /opt/Tanium/TaniumClient
```
- start service with `systemctl start taniumclient.service`
- check it's enabled and running  with `sudo systemctl status taniumclient`
- check configuration with `sudo /opt/Tanium/TaniumClient/TaniumClient config list`