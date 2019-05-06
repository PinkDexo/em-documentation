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

---

#### Configuration import

By default, the commerce configuration is included in all packages. To import the configuration, run drush command depending on the installation package you have used.

If you have composer managed **Drupal** or **Thunder** site, run:

```sh
drush cim -y --partial --source=../config/shop_config/
```

If you run standard Drupal site:

```sh
drush cim -y --partial --source=sites/default/config/shop_config/
```

If you have standard Thunder site:

```sh
drush cim -y --partial --source=configuration/thunder_config/shop_config/
```
