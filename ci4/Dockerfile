FROM php:7.4-apache

# Update and upgrade packages
RUN apt-get update && apt-get upgrade -y

# Install system dependencies required for intl extension
RUN apt-get install -y libicu-dev

# Install the MySQLi and intl extensions
RUN docker-php-ext-install mysqli intl

# Enable the installed extensions
RUN docker-php-ext-enable mysqli intl

# Clean up to reduce image size
RUN apt-get clean

# Apache configuration (optional)
# You can copy your Apache configuration files here, if needed.

# Start Apache
CMD ["apache2-foreground"]
