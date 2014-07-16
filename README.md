Boilerplate
===========

HTML5 Boilerplate BEdita frontend from http://www.initializr.com/

Setup
=====

a. Clone frontend boilerplate into local bedita frontend path, normally this is the __frontends__ folder inside bedita (like */var/www/bedita/frontends*), so:

```
      cd /var/www/bedita/frontends
      git clone git@github.com:bedita/boilerplate.git
```

b. Copy *boilerplate/webroot/index.php.sample* to *boilerplate/webroot/index.php*.


c. Copy *boilerplate/config/core.php.sample* to *boilerplate/config/core.php* and modify it, if necessary...


d. Set write permissions for temporary folder *boilerplate/tmp*.
    For example, in a unix shell, assuming 'john' is the username and current path is *frontends* folder:

```
      sudo chown -R john:www-data boilerplate/tmp
      sudo chmod -R g+w boilerplate/tmp
```

If something goes wrong take a look at log files (for example in *boilerplate/tmp/logs*) and tune your core.php file, changing debug level as needed (*boilerplate/config/core.php*).

Also read this article: http://docs.bedita.com/setup/if-something-goes-wrong-in-bedita


Note
====
If your frontend path is not inside *bedita/frontends* but elsewhere, you may edit *boilerplate/webroot/index.php* and set properly CAKE_CORE_INCLUDE_PATH and BEDITA_CORE_PATH.
For instance, if your bedita home path is /var/www/bedita:

```
      if (!defined('CAKE_CORE_INCLUDE_PATH')) {
            define('CAKE_CORE_INCLUDE_PATH', "/var/www/bedita");
      }

      if (!defined('BEDITA_CORE_PATH')) {
            define('BEDITA_CORE_PATH', "/var/www/bedita/bedita-app");
      }
```
