# Base on offical NGINX Alpine image
FROM nginx:1.25.2-alpine

# remove existing files from nginx directory
RUN rm -rf /usr/share/nginx/html/*
# Remove any existing config files
# RUN rm /etc/nginx/nginx.conf
RUN rm /etc/nginx/conf.d/*

# Copy config files
# *.conf files in conf.d/ dir get included in main config
COPY ./data/nginx /etc/nginx/conf.d/
COPY ./html /usr/share/nginx/html/
COPY ./data/certbot/conf /etc/letsencrypt
COPY ./data/certbot/www /var/www/certbot

# Expose the listening port
EXPOSE 80
EXPOSE 443

# Launch NGINX
CMD [ "nginx", "-g", "daemon off;" ]