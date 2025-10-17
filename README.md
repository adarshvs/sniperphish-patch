sudo apt install -y build-essential pkg-config libxml2-dev libsqlite3-dev libcurl4-openssl-dev libonig-dev libzip-dev libssl-dev libpng-dev libjpeg-dev libfreetype6-dev libxslt1-dev libreadline-dev libffi-dev libgmp-dev


wget https://www.php.net/distributions/php-8.1.29.tar.gz


tar -xvzf php-8.1.29.tar.gz


cd php-8.1.29


./configure --prefix=/usr/local/php8.1 --with-openssl --with-zlib --enable-mbstring --enable-bcmath --enable-ftp --enable-exif --enable-intl --enable-soap --enable-zip --with-curl --with-gettext --with-gd --with-mysqli --with-pdo-mysql --enable-fpm

make -j$(nproc)

sudo make install


sudo ln -sf /usr/local/php8.1/bin/php /usr/bin/php

php -v
