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


3. Import the configuration with **drush**:

If you import the configuration on a composer managed Drupal or Thunder site run:

```sh
cim -y --partial --source=../config/shop_config/
```

otherwise run:

```sh
drush cim -y --partial --source=sites/default/config/shop_config/
```

