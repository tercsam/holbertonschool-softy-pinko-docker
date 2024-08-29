# Utiliser l'image Nginx comme base
FROM nginx:latest

# Copier les fichiers du front-end dans le répertoire Nginx approprié
COPY ./softy-pinko-front-end /var/www/html/softy-pinko-front-end

# Copier la configuration personnalisée de Nginx
COPY ./softy-pinko-front-end.conf /etc/nginx/conf.d/default.conf

EXPOSE 9000

CMD ["nginx", "-g", "daemon off;"]