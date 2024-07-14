# Notes to install PHP on Ubuntu

Install PHP:

```
sudo apt update
sudo apt install php8.1-cli
php --version
```

Install Composer:

```
curl -sS https://getcomposer.org/installer -o /tmp/composer-setup.php
HASH=`curl -sS https://composer.github.io/installer.sig`
php -r "if (hash_file('SHA384', '/tmp/composer-setup.php') === '$HASH') { echo 'Installer verified'; } else { echo 'Installer corrupt'; unlink('composer-setup.php'); } echo PHP_EOL;"
sudo php /tmp/composer-setup.php --install-dir=/usr/local/bin --filename=composer
composer
```

Install the PHP cURL extension:

```
sudo apt-get install php8.1-curl
```

Install the PHP XML extension:

```
sudo apt-get install php8.1-xml
```