# Mikrotik IPBlacklist

## Script for autoupdate ip address blacklist.

- Run this code in terminal to create firewall rules

<code>/ip firewall filter\
add action=drop chain=input comment="Drop IP from Blacklist" in-interface=WAN \\
    log=yes log-prefix="Drop IP from Blacklist" src-address-list=\\
    "IP Blacklist"</code>

- Run this code in terminal to create autoupdate script.

<code>/system script\
add dont-require-permissions=no name=DownloadIpBlacklist \\
    policy=read,write \\
    source="/tool fetch address=raw.githubusercontent.com host=raw.githubuserc\\
    ontent.com mode=https src-path=/devMikeUA/MikrotikIpBlacklist/master/scrip\\
    t/IP_Blacklist.rsc"
</code>