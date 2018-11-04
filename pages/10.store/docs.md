---
title: Store
taxonomy:
    category:
        - docs
child_type: docs
---

##### The theme utilize **[Drupal Commerce](https://www.drupal.org/project/commerce)** module for it's store. 

! The Commerce modules uses 3rd party dependencies which can be managed only with Composer. If you don't plan to run shop on your site, I recommend you to uninstall all Commerce and Commerce related modules to prevent future issue while updating your Drupal core.

<hr>

##### To uninstall Drupal Commerce modules follow this steps:

**Step 1**: Delete all Commerce related entities:

1. Delete all orders (`/admin/modules/uninstall/entity/commerce_order`)
2. Delete all order items (`/admin/modules/uninstall/entity/commerce_order_item`)
3. Delete all payments (`/admin/modules/uninstall/entity/commerce_payment`)
4. Delete all payment methods (`/admin/modules/uninstall/entity/commerce_payment_method`)
5. Delete all product variations (`/admin/modules/uninstall/entity/commerce_product_variation`)
6. Delete all products (`/admin/modules/uninstall/entity/commerce_product`)
7. Delete all stores (`/admin/modules/uninstall/entity/commerce_store`)

**Step 2:** Uninstall modules

1. Go to: Administration > Extend and click on Uninstall tab (`/admin/modules/uninstall`)
2. Uninstall all Commerce modules
3. Uninstall Address module