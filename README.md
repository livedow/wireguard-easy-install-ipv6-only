sysctl.conf settings

# Enable IPv6 Forwarding
net.ipv6.conf.all.forwarding = 1
net.ipv6.conf.default.forwarding = 1

# Optional: Disable IPv4 completely if desired
net.ipv4.conf.all.forwarding = 0
net.ipv4.conf.default.forwarding = 0

Key Steps to Disable IPv4

    Modify Configuration (wg0.conf): Edit the server or client config file to remove IPv4 addresses from the [Interface] section and remove IPv4 ranges from [Peer] AllowedIPs.
    Use IPv6 Only: Ensure the Address field only contains an IPv6 address (e.g., Address = fd00::1/64) and AllowedIPs only includes IPv6 ranges (e.g., AllowedIPs = ::/0).
    Prevent Routing Changes: To prevent WireGuard from interfering with existing IPv4 routes on a client, add Table = off under the [Interface] section, as detailed in this Super User post.
    DNS Changes: Ensure that the DNS server specified in the config is an IPv6 address to prevent IPv4 DNS leakage. 
