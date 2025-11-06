# Dockerfile para el backend PHP/Laravel
FROM php:8.2-apache

# Instalar extensiones necesarias de PHP (PDO, MySQL)
RUN docker-php-ext-install pdo pdo_mysql mysqli

# Habilitar mod_rewrite para Laravel
RUN a2enmod rewrite

# Establecer el directorio de trabajo
WORKDIR /var/www/html

# Copiar el código al contenedor
COPY . .

# Ajustar permisos para carpetas de Laravel
RUN chown -R www-data:www-data /var/www/html/storage /var/www/html/bootstrap/cache
