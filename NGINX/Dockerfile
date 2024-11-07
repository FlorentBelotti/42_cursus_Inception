# version : latest stable
FROM debian:bullseye

# basic installation
RUN apt update && apt install -y nginx

# basic tools
RUN apt install -y vim && apt install -y curl

# TSL certificate
RUN mkdir -p /etc/nginx/ssl
RUN apt install -y openssl
RUN openssl req -x509 -nodes -out /etc/nginx/ssl/inception.crt -keyout /etc/nginx/ssl/inception.key -subj "/C=FR/ST=Paris/L=Paris/O=42/OU=42/CN=inception"

# Nginx configuration
RUN mkdir -p /var/run/nginx
COPY conf/nginx.conf /etc/nginx/nginx.conf

# Autorisation
RUN chmod 755 /var/www/html
RUN chown -R www-data:www-data /var/www/html

# Nginx launch
CMD [ "nginx", "-g", "daemon off;" ]