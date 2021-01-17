# firewalld
This is still a work in in progress so expect bugs or for things to not work!

## Depreciated!

I abandoned this role some time ago but i'm going to go ahead and finally archive it.  The reasons it was abandoned is due to flaws in the design of firewalld.  Zones, while appealing in theory, add a layer of complexity to firewall management that is more harmfull then helpfull.  To make matters worse when nftables is the firewalld backend the firewalld rules can be completely bypassed by other nftables tables.  firewalld has no builtin way to handle this and have stated it was done this way by design.  This is just my conjecture from experience working with firewalld, iptables, and nftables.

My reccomendation, with as little weight as it may have, is to reduce the complexity of your firewall and use iptables or nftables directly.  Both tools are easyer to take full control with ansible and, unlike firewalld, can act as the single source of truth for your host-based firewall.

## Offical firewalld documentation
- [firewalld toc](https://firewalld.org/documentation/)
- [zones](https://firewalld.org/documentation/zone/)
- [services](https://firewalld.org/documentation/service/)
- [ipsets](https://firewalld.org/documentation/ipset/)
- [nftables backend](https://firewalld.org/2018/07/nftables-backend)

## How To Use This Role


## Container/VM Technologies
### Docker Support
1. Create docker zone
2. Set target to 'ACCEPT'
3. Enable masquarade
4. add interface "docker0' to zone
5. test!

### Kubernetes Support?
