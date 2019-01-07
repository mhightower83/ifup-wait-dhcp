# Hmm, something has changed:
Something has changed since I originally had this problem.
Using `waitip 4` in `/etc/dhcpcd.conf` appears to now work for what I need.
If you are having problems with the Network not being up in time for services that require an interface with an ipv4 address, you should first try the above parameter.

I'll leave this here for a historical reference. The `dhcpcd.entry-hook` can be useful, if you need to update some information with the current IPv4 address.

# ifup-wait-dhcpcd
This work around applies to Raspbian. It attempts to force a delay on `network-online.target` being available, until we have an IP Address. Includes a 30 second timeout to avoid a possible hang on Network failure.
See [Wiki](https://github.com/mhightower83/ifup-wait-dhcp/wiki)
