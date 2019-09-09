---
title: 'Standard Thunder Installation'
published: false
menu: 'Standard Thunder Installation'
---

Thunder is a web-based open-source Content Management System based on Drupal 8. Thunder enabling its users to benefit from the Drupal community's continuous development efforts, as well as specific modules,  contributed by Hubert Burda Media, other publishers, and industry partners – the Thunder Coalition.

Thunder Website: [https://thunder.org/](https://thunder.org/)<br>
Thunder Project Page: [https://www.drupal.org/project/thunder](https://www.drupal.org/project/thunder)

<hr>

1. Download and unzip the [**Thunder**](https://www.drupal.org/project/thunder).
2. From Envato package unzip the **INSTALLATION/em-thunder.zip** and move **themes, modules, and libraries** to your Thunder root directory and **config** to your **sites/default** directory.
3. In the **sites/default** directory duplicate the **default.settings.php** file and rename it to **settings.php**.
4. Open the **settings.php** file with a text editor and add this line to the end of the file:

```php
$config_directories['sync'] = 'sites/default/config/sync';
```
    
5. Run Drush to install Thunder and EM from the configuration:

```sh
drush site:install thunder \
--existing-config \
--db-url=mysql://db_user:db_password@localhost/db_name  \
--account-name="demo" \
--account-pass="demo" \
--account-mail="your@email.com" \
thunder_module_configure_form.install_modules_thunder_demo=NULL
```

Change db_user, db_pass, and db_name with your database info. The --account-name is your Drupal username and the --account-pass your Drupal password. The last line "thunder_module_configure_form.install_modules_thunder_demo=NULL" tells the installer not to install Thunder demo content so you can install the EM Demo content later.


#### Install the demo content

To start with demo content, enable the **EM Thunder Demo** module:

```sh
drush en -y em_thunder_demo
```