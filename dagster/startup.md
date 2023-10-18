# Dagster Server Startup

Background Process settings:

`$ nohup dagster-webserver -h 0.0.0.0 -p 4444 -l /dagster &`
`$ $DAGSTER_HOME=<Project Folder> dagster-daemon run &`

NGINX settings:

```
server {
  listen 443 ssl;
  listen [::]:443;
  server_name code.kohaku.koi-hirajoshi.ts.net;
  ssl_certificate /etc/ssl/certs/kohaku.koi-hirajoshi.ts.net.crt;
  ssl_certificate_key /etc/ssl/certs/kohaku.koi-hirajoshi.ts.net.key;
  access_log  /var/log/nginx/kohaku.access.log;

   location /dagster/ {

    include proxy_params;
    proxy_set_header Host $host;
    proxy_set_header X-Real-IP $remote_addr;
    proxy_headers_hash_max_size 1024;
    proxy_headers_hash_bucket_size 128;
    proxy_set_header X-Forwarded-For $proxy_add_x_forwarded_for;

    proxy_http_version 1.1;
    proxy_set_header Upgrade $http_upgrade;
    proxy_set_header Connection "upgrade";
    proxy_read_timeout 86400;
    proxy_pass http://localhost:4444;
   }
}
