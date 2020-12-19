# based on https://github.com/docker-library/httpd/blob/master/2.4/alpine/Dockerfile

FROM httpd:2.4

# basic config file
COPY conf/httpd.conf /usr/local/apache2/conf/

# web space
COPY htdocs/missing.html /usr/local/apache2/htdocs
COPY htdocs/index.html /usr/local/apache2/htdocs

# configuration of virtual hosts
COPY conf/extra/httpd-vhosts.conf /usr/local/apache2/conf/extra
RUN mkdir -p /usr/local/apache2/htdocs/blog
RUN mkdir -p /usr/local/apache2/htdocs/wiki
COPY htdocs/blog/index.html /usr/local/apache2/htdocs/blog/
COPY htdocs/wiki/index.html /usr/local/apache2/htdocs/wiki/

# directory index
RUN mkdir -p /usr/local/apache2/htdocs/dir
