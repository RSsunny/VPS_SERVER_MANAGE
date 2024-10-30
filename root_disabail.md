## Root desable protection to hack

- To Get Access via SSH

```bash
ssh -p port_number username@IP
```

- if you don't create user then create a new user

````bash

## create a new user

```bash
sudo adduser user_name
````

- Grant Sudo Privileges (Optional): If you want the new user to have administrative privileges

```bash
sudo usermod -aG sudo new_user_name
```

- switch new user

```bash
su - new_user_name
```

### root disable

- Go to sshd_config file and change root permissions no

```bash
sudo nano /etc/ssh/sshd_config
```

### change root permission and save this file

- ssh restart

```bash
sudo service ssh restart
```
