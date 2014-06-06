Boilerplate
==========

Html5 Boilerplate BEdita frontend from http://intializr.com

Setup
=====

a. Clone frontend boilerplate into local bedita frontend path, normally this is the __frontends__ folder inside bedita (like __/var/www/bedita/frontends/boilerplate__), so:

```
      cd /var/www/bedita/frontends
      git clone git@github.com:bedita/boilerplate.git
```

b. Copy __boilerplate/webroot/index.php.sample__ to __boilerplate/webroot/index.php__.


c. Copy __boilerplate/config/core.php.sample__ into __boilerplate/config/core.php__ and modify it, if necessary...


d. Set write permissions for temporary folder __boilerplate/tmp__.
    For example, in unix shell, assuming 'john' is the username:

```
      sudo chown -R john:www-data /var/www/boilerplate/tmp
      sudo chmod -R g+w /var/www/boilerplate/tmp
```

Enjoy boilerplate frontend ;)

If something goes wrong take a look at log files (for example in boilerplate/tmp/logs) and tune your core.php file, changing debug level as needed (boilerplate/config/core.php).

Also read this article: http://docs.bedita.com/setup/if-something-goes-wrong-in-bedita


Note
====
If your frontend path is not inside /bedita/frontends, edit boilerplate/webroot/index.php and set properly CAKE_CORE_INCLUDE_PATH and BEDITA_CORE_PATH.
For instance, if your bedita home path is /var/www/bedita:

```
      if (!defined('CAKE_CORE_INCLUDE_PATH')) {
            define('CAKE_CORE_INCLUDE_PATH', "/var/www/bedita");
      }

      if (!defined('BEDITA_CORE_PATH')) {
            define('BEDITA_CORE_PATH', "/var/www/bedita/bedita-app");
      }
```
