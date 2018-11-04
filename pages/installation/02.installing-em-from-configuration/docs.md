---
title: 'Installing EM from Configuration '
media_order: install-from-config.jpg
taxonomy:
    category:
        - docs
---

Since Drupal 8.6 allows sites to be installed from an existing configuration, you can install the theme and all it's features using the EM configuration provided in the package.

### Manually

1. Move the content from the **em_drupal** directory to your web root location or to your development environment. Make sure that you copied all the files including hidden files like **.htaccess**
2. From the Envato package, unzip and move the **configuration/em_config** directory to your Drupal **sites/default** directory, so the path will be **sites/default/em_config**.
3. Make a copy of **sites/default/default.settings.php** and rename it to **settings.php**. 
4. Edit the **sited/default/settings.php** and set the configure sync directory location to point at **em_config** directory. To do that, add this line at the bottom of the settings.php file:

```php
$config_directories['sync'] = 'sites/default/em_config';
```

5. Visit your site in a web browser, choose **Language** and then choose "**Use existing configuration**"

![](install-from-config.jpg)

---

### Using Drush

This method shows how to install Drupal and EM theme from an existing configuration using Drush. This method requires [**Drush 9**](https://www.drush.org/).
If you already have Drush 8, you can install a site-local Drush 9 by running `composer require drush/drush` from your Drupal root directory. Otherwise, please refer to [Drush documentation](https://docs.drush.org/en/master/install/) page for more information on how to install Drush.

1. Move the content from the **em_drupal** directory to your web root location or to your development environment. Make sure that you copied all the files including hidden files like **.htaccess**
2. From the Envato package, unzip and move the **configuration/em_config** directory to your Drupal **sites/default directory**, so the path will be **sites/default/em_config**.
3. Make a copy of **sites/default/default.settings.php** and rename it to **settings.php**. 
4. Edit the **sited/default/settings.php** and set the configure sync directory location to point at **em_config** directory. To do that, add this line at the bottom of the settings.php file:

```php
$config_directories['sync'] = 'sites/default/em_config';
```

5. Run Drush site:install command:

```sh
drush site:install --existing-config --db-url=mysql://db_user:db_pass@localhost/db_name --account-name="demo" --account-pass="demo"
```
Change the **db_user**, **db_pass**, **db_host** and **db_name** with your database info. The **--account-name** is your Drupal username and the **--account-pass** is your Drupal password. This Drush command will install Drupal and will import EM configuration. 

! On production site, and if your account has permission to do so, it's a good idea to move the configuration sync directory outside of the webroot entirely. If you move the directory ouside of your web root, open up your settings.php file and change the sync location to: e.g. `$config_directories['sync'] = '../mysite/config/sync'`;