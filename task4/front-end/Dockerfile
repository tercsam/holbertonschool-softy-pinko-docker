# Use the latest version of Nginx as the base image
FROM nginx

# Copy the front-end files to the appropriate directory in the Nginx container
COPY ./softy-pinko-front-end /var/www/html/softy-pinko-front-end

# Copy the Nginx configuration file to the default configuration location
COPY ./softy-pinko-front-end.conf /etc/nginx/conf.d/default.conf

# Exposer le port 80
EXPOSE 8080

# Démarrer Nginx
CMD ["nginx", "-g", "daemon off;"]