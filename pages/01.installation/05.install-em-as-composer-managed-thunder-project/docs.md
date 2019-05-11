---
title: 'Install EM as composer-managed Thunder site'
taxonomy:
    category:
        - docs
menu: 'Composer-managed Thunder'
---

1. Unzip the **INSTALLATION/em-thunder-project.zip** to your development environment.
2. The package provides a **ready-made composer.json** file which will install all you need to kicks-start your composer-managed Thunder site. Run the `composer install` command from inside "**em-thunder-project**" directory.

```sh
cd em-drupal-project

composer install
```

Note that thunder-project installs Drupal itself in the "**docroot**" directory (**em-thunder-project/docroot**). Consider that on a production environment you have to configure your domain to point in that directory.

3. Use Drush and install the site form configuration. Run **drush site:install** from inside **docroot** directory:

```sh
cd docroot

../bin/drush site:install thunder \
--existing-config \
--db-url=mysql://db_user:db_password@localhost/db_name  \
--account-name="demo" \
--account-pass="demo" \
--account-mail="your@email.com" \
thunder_module_configure_form.install_modules_thunder_demo=NULL
```

Change db_user, db_pass and db_name with your database info. The --account-name is your Drupal username and the --account-pass your Drupal password. The last line "**thunder_module_configure_form.install_modules_thunder_demo=NULL**" tells the installer to not install Thunder demo content so you can install the EM Demo content later on.

4. If you'd like to start with a demo content, enable the **EM Thunder Demo** module:

```sh
../bin/drush en -y em_thunder_demo
```
---

This two articles will help you to understand how to manage your Drupal site with Composer:

Using Composer: [https://www.drupal.org/docs/develop/using-composer](https://www.drupal.org/docs/develop/using-composer) <br>
Drupal 8 Composer Best Practices: [https://www.lullabot.com/articles/drupal-8-composer-best-practices](https://www.lullabot.com/articles/drupal-8-composer-best-practices)
