A docker container where I play with Apache configuration. Do not ever use it in
production.

## Build
```bash
docker build -t httpd .
docker run -it -h sruby.com --add-host blog.sruby.com:172.17.0.2 --add-host wiki.sruby.com:172.17.0.2 httpd
```

## Test
```bash
curl -v -G http://sruby.com
curl -v -G http://www.sruby.com
curl -v -G http://blog.sruby.com
curl -v -G http://wiki.sruby.com
```
