# Bridge role

## What

> Bridge relays are Tor relays that are not listed in the public Tor directory.

~ https://support.torproject.org/censorship/censorship-7/

> This guide will help you set up an obfs4 bridge to help censored users connect to the Tor network. The requirements are:
> - 24/7 Internet connectivity
> - The ability to expose TCP ports to the Internet (make sure that NAT doesn't get in the way)

~ https://community.torproject.org/relay/setup/bridge/


## Why

Because the relays are not listed in the public Tor directory it is completely safe to run them on servers that are not fully utilized. I use this role to donate some of my bandwidth to others. 

## Managing

This script deploy the tor-bridge to `/opt/tor-bridge`.