---
title: Installation
taxonomy:
    category:
        - docs
---

To install EM shop, first you have to download and enable Drupal Commerce modules, then import EM Shop configuration. This procedure requires usage of Composer and Drush.

1. Use **Composer** to download Commerce modules. 

```sh
composer require drupal/commerce
```

2. Enable required commerce modules:

```sh
drush en -y commerce_checkout em_commerce_field_group
```

3. Unzip the **CONFIGURATION/shop_config.zip** from the Envato package and move the **shop_config** directory to your Drupal root directory.
4. Import the configuration with **drush** import command:

```sh
drush cim -y --partial --source=shop_config/
```

5. When import finish, you can remove the **shop_config** from your Drupal root.
