# Start with the latest version of the Nginx image
FROM nginx:latest

# Copy the front-end files to the Nginx web directory
COPY . /var/www/html/softy-pinko-front-end

# Copy the custom Nginx configuration file to replace the default
COPY ./softy-pinko-front-end.conf /etc/nginx/conf.d/default.conf
