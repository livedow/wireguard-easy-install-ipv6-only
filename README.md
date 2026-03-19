# sysctl.conf settings

    # Enable IPv6 Forwarding
    net.ipv6.conf.all.forwarding = 1
    net.ipv6.conf.default.forwarding = 1
    
    # Optional: Disable IPv4 completely if desired
    net.ipv4.conf.all.forwarding = 0
    net.ipv4.conf.default.forwarding = 0


**DNS Changes:** Ensure that the DNS server specified in the config is an IPv6 address to prevent IPv4 DNS leakage. 


