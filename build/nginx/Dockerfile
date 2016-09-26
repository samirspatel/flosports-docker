FROM nginx:latest

COPY symfony3.conf /etc/nginx/conf.d/symfony3.conf

RUN rm -rf /etc/nginx/conf.d/default.conf
RUN ln -sf /dev/stdout /var/log/nginx/access.log
RUN ln -sf /dev/stderr /var/log/nginx/error.log
RUN apt-get update && apt-get install php5-redis libxml2 zlib1g-dev -y --force-yes