# Docker 常用命令

## 1.编辑docker-compose.yml
```
vim docker-compose.yml
```
## 2.运行docker-compose.yml
```
docker compose up -d
```

# ❶Nav

```
version: '3'
services:
  nav-item:
    image: eooce/nav-item
    container_name: nav-item
    ports:
      - "3000:3000"
    environment:
      - PORT=3000
      - ADMIN_USERNAME=admin
      - ADMIN_PASSWORD=123456
    volumes:
      - ./database:/app/database
    restart: unless-stopped
```
# ❷StackEdit

```
version: "3.7"
services:
  stackedit:
    image: mafgwo/stackedit
    container_name: stackedit
    environment:
      - LISTENING_PORT=8080
      - DEBUG_FLAG=false
      - DROPBOX_APP_KEY=
      - DROPBOX_APP_KEY_FULL=
      - GITHUB_CLIENT_ID=
      - GITHUB_CLIENT_SECRET=
      - GITEE_CLIENT_ID=be63650f13e7223c7091d71bdf51a10588b7b9a75fc4bdb22002c89cae85cb93
      - GITEE_CLIENT_SECRET=1e87bcad48c613a32409e578fcab29a90255c4636d182bedf97e81e7667f3b35
      - GOOGLE_CLIENT_ID=
      - GOOGLE_API_KEY=
      - GITEA_CLIENT_ID=
      - GITEA_CLIENT_SECRET=
      - GITEA_URL=
      - GITLAB_CLIENT_ID=
      - GITLAB_CLIENT_SECRET=
    ports:
      - 8080:8080/tcp
    network_mode: bridge
    restart: always
```
