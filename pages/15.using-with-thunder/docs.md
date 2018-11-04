---
title: 'Using the Theme With Thunder Distribution'
taxonomy:
    category:
        - docs
menu: 'Drupal Thunder'
---

Thunder is a Drupal 8 distribution for professional publishing. It consists of the current Drupal 8 functionality, lots of handpicked publisher-centric modules with custom enhancements, and an environment which makes it easy to install, deploy and add new functionality.

About Thunder: https://www.drupal.org/case-study/thunder-the-drupal-8-distribution-for-professional-publishing
Download project: https://www.drupal.org/project/thunder


### Installing the Theme and Features on Thunder

1. Install the Thunder distribution
2. Copy modules and libraries from **ENVATO_PACKAGE/em_thunder** to to your Drupal Thunder root directory.
3. Copy themes from **ENVATO_PACKAGE/em_theme** to your Drupal Thunder theme directory.
4. Enable the EM Magazine theme and all EM required modules"

 - Statistics (statistics)
 - Custom Publishing Options (custom_pub)
 - Field formatter (field_formatter)
 - Masonry API (masonry)
 - Masonry Views (masonry_views)
 - Page Manager (page_manager)
 - Page Manager UI (page_manager_ui)
 - Panelizer (panelizer)
 - Panels (panels)
 - Panels IPE (panels_ipe)
 - Real name (realname)
 - Slick Views (slick_views)
 - Views Infinite Scroll (views_infinite_scroll)
 - Twig Field Value (twig_field_value)
 - Twig tweak (twig_tweak)
 - EM - Dynamic Teaser (em_dynamic_teaser)
 - EM Tweaks (em_tweaks)

You can run this Drush command to enable them all:

`drush en -y statistics custom_pub field_formatter field_formatter masonry masonry_views page_manager page_manager_ui panelizer panels realname slick_views twig_field_value twig_tweak views_infinite_scroll em_dynamic_teaser em_tweaks em_magazine`

5. Set **EM Magazine** as default theme

`drush cset -y system.theme default em_magazine`

! Note that the configuration import might fail if you have not enabled the EM Magazine theme, or some of the modules from above.


6. Import the EM configuration. The **ENVATO_PACKAGE/em_thunder/config** contains configuration files which you have to import in your Thunder distribution in order to bring in the EM functionalities.
Copy the "config" directory somewhere in you environment so it can be accessible for your terminal, then run this Drush command:

`drush cim -y --partial --source=YOUR_CONFIG_DIR_LOCATION/config`

7. After successful importing, you can set your [Front Page](/adjust-basic-site-settings#front-page) manualy, or with Drush. 

`drush cset -y system.site page.front /right-sidebar/two-columns-masonry`
