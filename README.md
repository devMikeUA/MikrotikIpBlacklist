# Mikrotik IPBlacklist

## Script for autoupdate ip address blacklist.

- Run this code in terminal to create firewall rules

<code>/ip firewall filter
add action=drop chain=input comment="Drop IP from Blacklist" in-interface=WAN \\
    log=yes log-prefix="Drop IP from Blacklist" src-address-list=\\
    "IP Blacklist"</code>

- Run this code in terminal to create autoupdate script.

<code>in progress</code>