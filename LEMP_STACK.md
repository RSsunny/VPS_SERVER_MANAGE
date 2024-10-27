## LEMP (Linux Nginx MySQL PHP) Stack

- Install Nginx

```bash
sudo apt install nginx
```

- Allow Nginx Firewall

```bash
sudo ufw allow 'Nginx Full'
```

- Install MySQL

```bash
sudo apt install mysql-server
```

- Install PHP

```bash
sudo apt install php-fpm php-mysql
```

- Check php is running

```bash
  sudo service php8.2-fpm
  OR
  sudo systemctl status php8.2-fpm
```

- Check Nginx status

```bash
sudo service nginx start
OR
sudo systemctl start nginx
```

- Test Nginx configuration

```bash
sudo nginx -t
```

- Restart Nginx

```bash
sudo systemctl restart nginx
```
