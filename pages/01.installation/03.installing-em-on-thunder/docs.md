---
title: ' Installing EM on Thunder'
taxonomy:
    category:
        - docs
---

Thunder is a web-based open-source Content Management System setting new standards for publishers’ CMS. It is based on Drupal 8, enabling its users to benefit from the Drupal community's continuous development efforts, as well as specific modules contributed by Hubert Burda Media, other publishers and industry partners – the Thunder Coalition.

Thunder Website: [https://thunder.org/](https://thunder.org/)<br>
Thunder Project Page: [https://www.drupal.org/project/thunder](https://www.drupal.org/project/thunder)

<hr>

Installing TheMAG on Thunder requires **Drush**.

1. Download and install [**Drupal Thunder**](https://www.drupal.org/project/thunder).
2. From the Envato package, move all directories from **em_thunder** to your Drupal Thunder root directory.
4. Use Drush to enable the theme and required modules.

```sh
drush en -y \
  statistics \
  custom_pub \
  field_formatter \
  masonry \
  masonry_views \
  page_manager \
  page_manager_ui \
  panelizer \
  panels \
  panels_ipe \
  realname \
  slick_views \
  views_infinite_scroll \
  comment \
  poll \
  search \
  block_content \
  em_dynamic_teaser \
  em_tweaks \
  em_magazine
```

5. Enable EM Magazine theme

```sh
# Note: Check your Drush version (drush --version) and use an appropriate command to enable the theme:

# If you have Drush 8+ run:
drush en -y em_magazine

# If you have Drush 9+ run:
drush theme:enable em_magazine
```

6. Set EM as default theme

```sh
drush cset -y system.theme default em_magazine
```

7. Clear Drupal cache

```sh
drush cr
```

8. Import the EM configuration

```sh
 drush cim -y --partial --source=configuration/thunder_config/
```

9. Set /combo/6 as a default front page

```sh
drush cset -y system.site page.front /combo/6
```

10. When you're done, you can remove the **configuration** directory from a Drupal root.

