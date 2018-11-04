---
title: 'Update Instructions'
---

#### EM 1.3.0

Coming up...

#### EM 1.2.2

1. Replace **themes/em** with **em** theme from the Envato package located in the em_theme directory.
2. Clear the Drupal cache
3. The theme does not require [Twig Tweak](https://www.drupal.org/project/twig_tweak) and [Twig Field Value](https://www.drupal.org/project/twig_field_value) modules anymore. If you don't use this two modules for other purpose, it is safe to uninstall and remove them.
4. Edit the **HTML Out** field on all **(EM) Featured Slider** views and remove the "**justify-content-center**" class from the first element. <br>Or, replace the first line  `<div class="content-wrapper d-flex justify-content-center align-items-center">` with `<div class="content-wrapper d-flex flex-row align-items-center">`

