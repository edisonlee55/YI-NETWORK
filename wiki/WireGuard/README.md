# How to using WireGuard to config a BGP Session

Notice: You need a routing software to set a BGP Session, [WireGuard](https://wireguard.com/) just a VPN Tunnel. But we use it to make site to site network.

This Demo System is working on Ubuntu

## Peer To Peer IP Address

If you are a novice of WireGuard, you should have use wg-quick.

But it's not working for peer to peer IP Address.
So, we need to use ```ip addr``` and ```ip link``` command to set

For example, if A is 10.121.211.254, B is 10.121.212.254

We will use this command in A

```ip addr add 10.121.211.254/32 peer 10.121.212.254/32 dev <interface>```

Corresponding, B should change IP Address of the servers on both ends
