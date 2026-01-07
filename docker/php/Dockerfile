FROM php:8.2-apache

# Mengaktifkan modul rewrite pada Apache
RUN a2enmod rewrite

# Memasang ekstensi PHP yang umum digunakan untuk aplikasi PHP native
RUN docker-php-ext-install mysqli pdo pdo_mysql

# Menyalin konfigurasi virtual host Apache
COPY vhost.conf /etc/apache2/sites-available/000-default.conf

# Menyalin konfigurasi PHP kustom
COPY php.ini /usr/local/etc/php/

# Menetapkan direktori kerja aplikasi
WORKDIR /var/www/html
