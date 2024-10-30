## How to install phpmyadmin with Nginx

- instal phpmyadmin and others plugins

```bash
sudo apt install phpmyadmin php-mbstring php-zip php-gd php-json php-curl
```

- create symlink

```bash
sudo ln -s /usr/share/phpmyadmin /var/www/project_folder_name/phpmyadmin
```

### if forbidden error show your computer then follow the instructions

- Check Permissions

```bash
sudo chown -R www-data:www-data /usr/share/phpmyadmin
sudo chmod -R 755 /usr/share/phpmyadmin
```

- Verify Nginx Configuration

```bash
sudo nano /etc/nginx/sites-available/default
```

### past thes code here

```bash
location /phpmyadmin {
    alias /usr/share/phpmyadmin;
    index index.php index.html index.htm;
}
```

- Restart Nginx

```bash
sudo systemctl restart nginx
```

- If you’re using PHP-FPM, make sure Nginx is configured to process .php files correctly. The configuration file should include something like

```bash
location ~ \.php$ {
    include snippets/fastcgi-php.conf;
    fastcgi_pass unix:/var/run/php/php8.1-fpm.sock;
}
```

- Restart Nginx

```bash
sudo systemctl restart nginx

```

## check again your apiaddress/phpmyadmin

### Note

- php-mbstring: A module for managing non-ASCII strings with different encodings
- php-zip: An extension that facilitates uploading .zip files to phpMyAdmin
- php-gd: Enables support for GD graphics library
- php-json: Provides support for JSON serialization
- php-curl: Allows PHP to communicate with other servers

### If get warning e.g. "The $cfg['TempDir'] (/var/lib/phpmyadmin/tmp/) is not accessible." then run below commands

```bash
cd /var/lib/phpmyadmin
sudo chmod -R 775 tmp
sudo service nginx restart
```
