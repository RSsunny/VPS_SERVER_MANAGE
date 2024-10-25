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

- log any error check use pm2

```bash
pm2 log
```

```bash
pm2 log app_name/id
```

- delete project

```bash
pm2 delete app_name/id/all
```

- stop project

```bash
pm2 stop app_name/id/all
```

- monito your sit

```bash
pm2 monit
```

## you can do add link for monitoring with pm2 premium

- register acount pm2 monitor
- create new project
- link up your server

```bash
 pm2 link your link

```
