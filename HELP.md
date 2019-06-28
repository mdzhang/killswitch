See traffic on network device:

```sh
# shouldn't see much here
$ NW_DEVICE=$(netstat -i | tail -1 | awk '{print $1}')
$ sudo tcpdump -i $NW_DEVICE
# mostly lines reading e.g. $(hostname).60090 > IP $VIP_IP

# everything should really be on VPN
$ NW_TUN="tun0"
$ sudo tcpdump -i $NW_TUN
```
