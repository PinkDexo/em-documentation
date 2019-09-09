---
title: 'Update Instructions'
---

! Always test updates on a non production environment!

 #### EM 1.3.6
 
There are no changes made on the base theme, so you don't have to replace it. The sub-theme "em_magazine" includes boilerplate template files that can help to adjust the theme for your custom content types.


 #### EM 1.3.5

1. Replace the "em" theme located in your theme directory (`themes/em`) with **THEME/em** from the Envato package.
2. Go to Performance page and clear the cache (`/admin/config/development/performance`)


#### EM 1.3.4

1. Replace the "em" theme located in your theme directory (`themes/em`) with **THEME/em** from the Envato package.
2. Go to Performance page and clear the cache (`/admin/config/development/performance`)


#### EM 1.3.3

1. Replace the "em" theme located in your theme directory (`themes/em`) with **THEME/em** from the Envato package.
2. Go to Performance page and clear the cache (`/admin/config/development/performance`)

#### EM 1.3.2

1. Replace the "em" theme located in your theme directory (`themes/em`) with **THEME/em** from the Envato package.
2. Go to Performance page and clear the cache (`/admin/config/development/performance`)

#### EM 1.3.1

1. Replace the "em" theme located in your theme directory (`themes/em`) with **THEME/em** from the Envato package.
2. Go to Performance page and clear the cache (`/admin/config/development/performance`)

#### EM 1.3.0

1. In your Drupal theme directory, replace  **em** (`themes/em`) with **em** theme from the Envato package located in **other/theme_only/em**.
2. Go to Performance page and clear the cache (`/admin/config/development/performance`)
3. In order to improve responsive flexibility on grid layouts, the theme now use Bootstrap responsive variations on grid--N classes. This change will affect all Views with grid layouts. To make your grids responsive again, you have to change **Wrapper class** under **Format  / Settings** in the View,  according [this example](https://docs.em.pinkdexo.com/views-and-teasers/create-a-view-from-scratch#responsive-variations).
4. If you'd like to use new Featured Grids on your site, use the Configuration manager to import the Views.

  1. Go to Configuration synchronization page and choose to import Single Item. (`/admin/config/development/configuration/single/import`) 
  2. From **Configuration type** dropdown, select **View**
  3. Paste a certain View configuration from the table below and click **Import**
  4. To add a Featured grid layout on your page follow [Add New Block](https://docs.em.pinkdexo.com/pages/managing-page-layouts#add-new-block) instructions. You will fond **Featured grid** block under **(EM) Featured** category.

<br>

  | View | Configuration |
  | ---- | ------------- |
  |Featured grid 1 ([preview](https://em.pinkdexo.com/featured-grid/1)) | [Click here and copy the configuration](https://gist.github.com/PinkDexo/de0953faa76793c6a905b3e18eb987f5) |
  |Featured grid 2 ([preview](https://em.pinkdexo.com/featured-grid/2)) | [Click here and copy the configuration](https://gist.github.com/PinkDexo/39ab9491adcfb230a95f9270d7b8ed1d) |
  |Featured grid 3 ([preview](https://em.pinkdexo.com/featured-grid/3)) | [Click here and copy the configuration](https://gist.github.com/PinkDexo/ac2eecee3753f3f4c678c682cc53be21) |

---

#### EM 1.2.2

1. Replace **themes/em** with **em** theme from the Envato package located in the em_theme directory.
2. Clear the Drupal cache
3. The theme does not require [Twig Tweak](https://www.drupal.org/project/twig_tweak) and [Twig Field Value](https://www.drupal.org/project/twig_field_value) modules anymore. If you don't use this two modules for other purpose, it is safe to uninstall and remove them.
4. Edit the **HTML Out** field on all **(EM) Featured Slider** views and remove the "**justify-content-center**" class from the first element. <br>Or, replace the first line  `<div class="content-wrapper d-flex justify-content-center align-items-center">` with `<div class="content-wrapper d-flex flex-row align-items-center">`

