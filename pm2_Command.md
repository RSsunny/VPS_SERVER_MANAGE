## PM2 - Advanced, production process manager for Node.JS

- install

```bash
sudo npm install -g pm2@latest
```

- version check

```bash
pm2 --version
```

- PM2 Process on Startup

```bash
sudo pm2 startup
```

### start node js project use pm2

```bash
pm2 start ecosystem.config.js
```

- save pm2 process

```bash
pm2 save
```

- check status

```bash
pm2 status
```

- list all project running

```bash
pm2 list
```

### when update project then reload pm2 process

```bash
pm2 reload app_name/id
```
