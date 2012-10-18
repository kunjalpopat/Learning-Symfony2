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
    -> short_open_tag = Off 
    -> magic_quotes_gpc = Off 
    -> register_globals = Off 
    -> session.autostart = Off
   
=> sudo apt-get install libssl-doc [If not installed in System then install]

============== PROBLEM IN INSTALLATION THEN USE BELOW INSTRUCTIONS FOR THIS =================
=> sudo gedit /etc/apt/preferences

and insert the following lines:

Package: *       

Pin: release a=precise*

Pin-Priority: 2012

Pin-Priority must be greater than 1000.
==============================================================================================

Then you may downgrade the offending applications with:

=> sudo apt-get dist-upgrade [if u want]

Then you may install packages that complained about dependencies, like sudo apt-get install ia32-libs-multiarch, or sudo apt-get install ia32-libs.

=> sudo apt-get install libssl-doc
=> sudo apt-get install libicu-dev
=> sudo apt-get install php5-intl

==================================== REMOVE THIS ============================================

Finally, you should remove the file you just created:

=> sudo rm /etc/apt/preferences

=============================================================================================

After you will Start your Symfony2 and see on URL: http://localhost/Symfony/web/config.php

Message : Your configuration looks good to run Symfony.