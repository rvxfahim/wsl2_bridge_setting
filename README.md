# wsl2_bridge_setting

## .wslconfig

[wsl2]

kernelCommandLine=ipv6.disable=1

memory=16GB

swap=0

guiApplications=true

debugConsole=false

#vmIdleTimeout=-1


networkingMode=bridged

vmSwitch=WSLBridged

dhcp=false

macAddress=0E:00:00:00:00:00

ipv6=false


[experimental]

autoMemoryReclaim=gradual

## And inside ubuntu distro:

### /etc/wsl.conf

[user]

default=gittu

[boot]

systemd=true

[network]

hostname = GITTUW11WSL

generateResolvConf=false

## /etc/systemd/network/20-wslbridged.network

[Match]

Name=eth0


[Network]

Description=WSLBridged

DHCP=yes

