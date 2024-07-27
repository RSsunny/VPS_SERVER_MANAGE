### How to access server via ssh and setup ssh key for passwordless authentication

Without setting up SSH Key It will ask Password each time we try to get access

- To Get Access via SSH

#### Note:- Run Below Commands on Your Local Machine, Not on Your VPS or Remote Server

- Generate SSH Key

```sh
ssh-keygen -t rsa -b 4096
```

### Copy SSH Public Key to Remote Server

### login root user your vps server and check your root directory have .ssh folder. if you don't have .ssh folder now create a new folder then go to then .ssh folder and create a new file authorized_keys and past public key follow this command

- login root user

```sh
Syntax:- ssh root@ip_address
- yoyr password
```

- check your root directory and .ssh

```sh
- pwd (/root)
```

- if you want to .ssh folder

```sh
- mkdir .ssh
```

- past public key create a new file authorized_keys

```sh
- cd .ssh
- sudo nano authorized_keys
```

```sh
- exit
```

### again login root user no need password auto login root
