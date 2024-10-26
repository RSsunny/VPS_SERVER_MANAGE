## These commands work with most Linux distributions (such as Ubuntu and CentOS), though the package manager commands (apt for Debian/Ubuntu or yum for CentOS/RHEL) may vary slightly.

- install Nginx

```bash
sudo apt install nginx
```

- Version check

```bash
nginx -v
```

- If you want to allow ufw

```bash
sudo ufw allow 'Nginx Full'
```

- Start Nginx

```bash
sudo systemctl start nginx
```

- Stop Nginx

```bash
sudo systemctl stop nginx
```

- Restart Nginx

```bash
sudo systemctl restart nginx
```

- Reload Nginx for configuration changes

```bash
sudo systemctl reload nginx
```

- Enable Nginx

```bash
sudo systemctl enable nginx
```

- Disable Nginx

```bash
sudo systemctl disable nginx
```

- Check Nginx status

```bash
sudo systemctl status nginx
```

- check Nginx configuration syntax

```bash
sudo nginx -t
```

- Edit Nginx main configuration file

```bash
sudo nano /etc/nginx/nginx.conf
```

- Edit Site specific configuration files

```bash
sudo nano /etc/nginx/sits-available/domain.com
```

### into the file past this command and replace your domain name and port number

```bash
server{
    listen 80;
    listen [::]:80;
    server_name your_domain www.your_domain;
    location / {
       proxy_pass http://localhost:3001;
       proxy_http_version 1.1;
       proxy_set_header Upgrade $http_upgrade;
       proxy_set_header Connection 'upgrade';
       proxy_set_header Host $host;
       proxy_cache_bypass $http_upgrade;
    }
}

```

- Enable site specific configuration files

```bash
sudo ln -s /etc/nginx/sites-available/domain.com /etc/nginx/sites-enabled/domain.com
```

- Disable site

```bash
sudo rm /etc/nginx/sites-enabled/domain.com
```

- Test Configuration and Reload Nginx

```bash
sudo nginx -t && sudo systemctl reload nginx

```

### If you need more information please visit documentation

- [Nginx Documentation](https://ubuntu.com/tutorials/install-and-configure-nginx#1-overview)
