Learning-Symfony2
=================

Required Modules installation and php.ini settings for running Symfony2, 

=> Download Symfony2 package

=> Extract in your webdata/root folder and give name Symfony

=> Open Terminal/Command Line and go to project directory

=> First Download and Install Composer for Project Dependancies fire below commands

    -> curl -s http://getcomposer.org/installer | php
    -> php composer.phar install
    -> sudo apache2ctl restart
=> sudo apt-get install php-apc [Install module for Alternative PHP Cache]

=> sudo apt-get install libicu-dev [Install package for  International Components for Unicode]

=> sudo apt-get install php5-suhosin [Install package for Advanced Protection System]

=> Add OR Edit below settings in php.ini [sudo gedit /etc/php5/apache2/php.ini] [sudo gedit /etc/php5/cli/php.ini]
   
   -> suhosin.executor.include.whitelist=”phar”
   -> date.timezone = UTC
   -> short_open_tag = Off, 
   -> magic_quotes_gpc = Off, 
   -> register_globals = Off, 
   -> session.autostart = Off
   



