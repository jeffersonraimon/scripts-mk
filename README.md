# scripts-mk 

### Script NTPv6 (RouterOSv7)

Put this on IPV6 > Firewall > Mangle (changing the addressess)

/ipv6 firewall mangle add action=snpt chain=postrouting comment=SNPT-s dst-prefix=2001:db8:4846:d801::/64 out-interface=WAN src-address=fd10:1:10::/64 src-prefix=fd10:1:10::/64

/ipv6 firewall mangle add action=dnpt chain=prerouting comment=DNPT-s dst-address=2001:db8:4846:d801::/64 dst-prefix=fd10:1:10::/64 in-interface=WAN src-prefix=2001:db8:4846:d801::/64
