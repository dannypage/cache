# Install Cockpit

## Why?

Easy UI for server management. 

Scratch that, the Nginx setup with HTTPS was a pain, look at Webmin.

## How

In Ubuntu: 

```
. /etc/os-release
sudo apt install -t ${VERSION_CODENAME}-backports cockpit
```

View panel at <hostname>:9090.

## Other possibilities

[Webmin](https://webmin.com/)
