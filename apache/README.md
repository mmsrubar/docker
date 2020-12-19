A docker container where I play with Apache configuration. Do not ever use it in
production.

## Build
docker build -t httpd . \pagebreak
docker run -it -h sruby.com --add-host blog.sruby.com:172.17.0.2 --add-host wiki.sruby.com:172.17.0.2 httpd \pagebreak

## Test
curl -v -G http://sruby.com \pagebreak
curl -v -G http://www.sruby.com \pagebreak
curl -v -G http://blog.sruby.com \pagebreak
curl -v -G http://wiki.sruby.com \pagebreak
