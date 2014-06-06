boilerplate
==========

html5 boilerplate template frontend from intializr.com

setup
=====

Clone frontend responsive into local bedita frontend path, for example in /frontends folder inside bedita (like /var/www/bedita/frontends/boilerplate).

      cd /var/www/bedita/frontends
      git clone git@github.com:bedita/boilerplate.git

Copy boilerplate/webroot/index.php.sample in boilerplate/webroot/index.php.

If your frontend path is not inside /bedita/frontends, edit boilerplate/webroot/index.php and set properly CAKE_CORE_INCLUDE_PATH and BEDITA_CORE_PATH.
For instance, if your bedita home path is /var/www/bedita:

      if (!defined('CAKE_CORE_INCLUDE_PATH')) {
            define('CAKE_CORE_INCLUDE_PATH', "/var/www/bedita");
      }

      if (!defined('BEDITA_CORE_PATH')) {
            define('BEDITA_CORE_PATH', "/var/www/bedita/bedita-app");
      }

Copy config/core.php.sample into config/core.php:

      cd /var/www/bedita/frontends/boilerplate/config
      cp core.php.sample core.php

Set permits for temporary folder boilerplate/tmp.
For example, in unix shell, assuming 'john' is the username:

      sudo chown -R john:www-data /var/www/boilerplate/tmp
      sudo chmod -R g+w /var/www/boilerplate/tmp

Enjoy boilerplate frontend ;)

If something goes bad, take a look on logs (for example in /var/www/boilerplate/tmp/logs) and tune your core.php file, to change debug level as needed (/var/www/boilerplate/config/core.php).
