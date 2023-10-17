# Code Server

## Why?

For a remote coding IDE. Very much VS Code like.

## How?

TK adding install info

Via tailscale, do this stuff. Pay attention to what directories it's in, and possibly ending slashes.

```
server {
  listen 443 ssl;
  listen [::]:443;
  server_name code.kohaku.koi-hirajoshi.ts.net;
  ssl_certificate /etc/ssl/certs/kohaku.koi-hirajoshi.ts.net.crt;
  ssl_certificate_key /etc/ssl/certs/kohaku.koi-hirajoshi.ts.net.key;
  access_log  /var/log/nginx/kohaku.access.log;

  location /code {

    rewrite /code/(.*) /$1 break;

    proxy_pass http://100.125.191.133:1337/;
    proxy_set_header Host $host;
    proxy_set_header Upgrade $http_upgrade;
    proxy_set_header Connection upgrade;
    proxy_set_header Accept-Encoding gzip;
  }
```
