## If you want to login to new server then follow below commands

- use powershell your local computer

```bash
ssh root@ip_address
```

- update server

```bash
apt update
```

```bash
apt upgrade -y
```

## create a new user

```bash
sudo adduser user_name
```

- Grant Sudo Privileges (Optional): If you want the new user to have administrative privileges

```bash
sudo usermod -aG sudo new_user_name
```

- switch new user

```bash
su - new_user_name
```

- update new user server

```bash
sudo apt update
```

```bash
sudo apt upgrade -y
```

- check directory new user

```bash
pwd
```

- show all folders

```bash
ls -a
```

- create new folder

```bash
mkdir folder_name
```

- move to folder

```bash
cd folder_name
```

```bash
cd ~/folder_name
```

## you can write text use nano

- go to folder directory then

```bash
sudo nano file_name
```

### save this file crtl+X then Y then inter

- check install npm, node, git, pm2

```bash
nginx -v
node -v
npm -v
git --version
pm2 --version
```

- install doftware if you need

```bash
sudo apt install nginx
sudo apt install git
curl -fsSL https://deb.nodesource.com/setup_18.x | sudo -E bash - &&\
sudo apt-get install -y nodejs
```

- Nginx verify Active and Running

```bash
sudo service nginx status
```

- check ufw (Verify Web Server Ports are Open and Allowed through Firewall)

```bash
sudo ufw status verbose
```

### install pm2

- [Go pm2 file](pm2_Command.md)

### logout vps server

```bash
exit
```
