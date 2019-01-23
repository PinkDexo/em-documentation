---
title: 'Install EM as composer-managed Drupal project'
taxonomy:
    category:
        - docs
menu: 'Composer-managed Drupal'
---

1. Unzip the **INSTALLATION/em-drupal-project.zip** to your development environment.
2. The package provides a **ready-made composer.json** file which will install all you need to kicks-start your composer-managed site. Run the `composer install` command from inside "**em-drupal-project**" directory.

```sh
cd em-drupal-project

composer install
```

Note that drupal-project installs Drupal itself in the "**web**" directory (**em-drupal-project/web**). Consider that on a production environment you have to configure your domain to point in that directory.

3. Use Drush and install the site form configuration. Run **drush site:install** from inside **web** directory:

```sh
cd web

drush site:install \
  --existing-config  \
  --db-url=mysql://db_user:db_pass@localhost/db_name \
  --account-name="demo" \
  --account-pass="demo" \
  --account-mail="your@mail.com" \
```

Change the db_user, db_pass and db_name with your database info. The --account-name is your Drupal username and the --account-pass your Drupal password. This Drush command will install Drupal and import the configuration.

4. If you'd like to start with a demo content, enable the **EM Demo** module:

```sh
drush en -y em_demo_content
```

If you are not familiar with Using Composer with Drupal, you can start from here:

Composer: https://www.drupal.org/docs/develop/using-composer
Drupal 8 Composer Best Practices: https://www.lullabot.com/articles/drupal-8-composer-best-practices
