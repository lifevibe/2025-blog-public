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
