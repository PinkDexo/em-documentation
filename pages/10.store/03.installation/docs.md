---
title: Installation
taxonomy:
    category:
        - docs
---

To install EM shop, first you have to download and enable Drupal Commerce modules, then import EM Shop configuration. This Procedure requires usage of Composer and Drush.

1. Run the **Composer** from your Drupal root directory to download the Commerce modules:

```sh
composer require drupal/commerce
```

2. Enable required commerce modules:

```sh
drush en -y commerce_checkout em_commerce_field_group
```

3. Unzip and move the "**shop_config**" directory, located in the **configuration** directory in Envato package to your Drupal root directory.
4. Import the configuration with Drush:

```sh
drush cim -y --partial --source=shop_config/
```

5. When the import finish, you can remove the **shop_config** directory from the Drupal root.
