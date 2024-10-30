## Change Default PORT number

- log in server

```bash
ssh -p port_number username@IP
```

- change default port number

```bash
sudo nano /etc/ssh/sshd_config
```

### change prot number or write new port number then save file ctrl+x then Y then Inter

- restart ssh

```bash
sudo service ssh restart
```
