
### In Client side (Laptop) : in Wireguard.app :
**[Interface]**

**PrivateKey** = .......

**Address** = 10.0.0.2/24

**DNS** = 1.1.1.1


**[Peer]**

**PublicKey** = ........

**AllowedIPs** = 0.0.0.0/0, ::/0

**Endpoint** = 35.209.195.224:41287

**PersistentKeepalive** = 25


### On Server side (VM) : when done sudo wg :
this should show 
```sh
interface: wg0
  public key: ..........
  private key: (hidden)
  listening port: 41287

peer: ..........
  endpoint: 49.37.171.111:59122
  allowed ips: 10.0.0.2/32
  latest handshake: 1 minute, 23 seconds ago
  transfer: 6.94 MiB received, 29.88 MiB sent
```

For restarting :
```shell
sudo systemctl restart wg-quick@wg0
```




