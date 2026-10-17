# Install / verify notes

1. Confirm Linux distro, VPS public IP, UDP 51820 availability and the actual game transport/port.
2. Install WireGuard using the VPS provider's supported method.
3. Generate keys on the server/client; never commit private keys to GitHub.
4. Configure IPv4 forwarding and narrow firewall/NAT rules only after confirming the egress interface and server topology.
5. Open the WireGuard UDP port in both host firewall and provider firewall.
6. Test the tunnel handshake first, then test routing to the game endpoint.
7. Keep a rollback path. Do not flush firewall rules or replace the host's existing rules wholesale.

A route to `185.207.214.14/32` only sends traffic for that IP through the tunnel. It does not rewrite the official game's server list or make the game choose this IP.
