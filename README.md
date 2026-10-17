
# FunRussia Game Tunnel

WireGuard tunnel prototype for iPhone connectivity testing.

## Required deployment settings

- Docker runtime with WireGuard support
- NET_ADMIN capability
- Accessible inbound UDP port 51820
- IP forwarding and NAT/routing support
- Public SERVERURL pointing to the actual WireGuard endpoint

## Game destination

185.207.214.14:7785

The iPhone peer is configured to route the game server IP
through the tunnel using ALLOWEDIPS=185.207.214.14/32.

## Important

A successful image build does not prove that the tunnel works.
The host must support WireGuard networking and inbound UDP.
Verify the actual game transport protocol and test the connection
from an iPhone before announcing availability to players.
