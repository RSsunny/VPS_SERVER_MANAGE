## UFW (Uncomplicated Firewall) is presented as a front-end of Iptables. By default, UFW denies all incoming connections and allows all outgoing connections.

- To Get Access via SSH

```bash
ssh -p port_number username@IP
```

- Install ufw

```bash
sudo apt install ufw
```

- Allow SSh connections

```bash
sudo ufw allow ssh
```

- If SSH is on a different port (e.g., 2222)

```bash
sudo ufw allow 2222/tcp
```

- Allow Other Necessary Ports:

```bash
sudo ufw allow 80/tcp    # HTTP
sudo ufw allow 443/tcp   # HTTPS

```

- Enable UFW

```bash
sudo ufw enable
```

- Verify UFW Status

```bash
sudo ufw status
```

- Delete specifie number

```bash
sudo ufw delete 4
```

- Disable UFW (if needed)

```bash
sudo ufw disable
```
