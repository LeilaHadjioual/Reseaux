
###PROCEDURE INSTALLATION

    1  apt-get update  
    2  apt-get upgrade  
    3  apt-get install apache2  
    4  service apache2 start  
    5  apt-get install php  
    6  php -v  
    7  service apache2 restart  
    8  cd /var/www/html/  
    9  ls  
    10  vi index.html   
    11  apt-get install vim  
    12  ls
    13  vi index.html 
    14  vi toto.php
    15  cd
    16  apt-get install mariadb-common mariadb-server mariadb-client
    17  service mysql start
    18  mysql
    19  apt-get install phpmyadmin
    20  service apache2 restart
    21  cd /var/www/
    22  git clone https://github.com/Ser-Custodio/Laravel_Cafe.git
    23  apt-get install git
    24  git clone https://github.com/Ser-Custodio/Laravel_Cafe.git
    25  ls
    26  cd Laravel_Cafe/
    27  ls
    28  cd /etc/apache2/sites-available/
    29  ls
    30  cp 000-default.conf 
    31  cp 000-default.conf sergio.conf
    32  vi sergio.conf 
    33  a2ensite sergio.conf
    34  service apache2 reload
    35  cd
    36  cd /var/log/apache2/
    37  ls
    38  ls -rtlh
    39  tail error.log 
    40  cd /var/www/Laravel_Cafe/
    41  ls
    42  composer install
    43  php -r "copy('https://getcomposer.org/installer', 'composer-setup.php');"
    44  php -r "if (hash_file('SHA384', 'composer-setup.php') === '544e09ee996cdf60ece3804abc52599c22b1f40f4323403c44d44fdfdd586475ca9813a858088ffbc1f233e9b180f061') { echo 'Installer verified'; } else { echo 'Installer corrupt'; unlink('composer-setup.php'); } echo PHP_EOL;"
    45  php composer-setup.php
    46  php -r "unlink('composer-setup.php');"
    47  ls
    48  php ./composer.phar install
    49  tail /var/log/apache2/error.log 
    50  ls
    51  chmod -R a+w storage/
    52  tail /var/log/apache2/error.log 
    53  ls
    54  tail storage/logs/laravel.log 
    55  less storage/logs/laravel.log 
    56  php artisan key:generate
    57  ls
    58  ls -a
    59  cp .env.example .env
    60  vi .env
    61  php artisan key:generate
    62  vi .env
    63  a2enmod rewrite
    64  vi public/.htaccess 
    65  service apache2 restart
    66  vi /etc/apache2/sites-available/sergio.conf 
    67  service apache restart
    68  service apache2 restart
    69  history
    70  history > public/history.txt