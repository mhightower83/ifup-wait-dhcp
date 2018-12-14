# ifup-wait-dhcpcd
This work around applies to Raspbian. It attempts to force a delay on `network-online.target` being available, until we have an IP Address. Includes a 2 minute timeout to avoid a possible hang on Network failure.
See [Wiki](https://github.com/mhightower83/ifup-wait-dhcp/wiki)
