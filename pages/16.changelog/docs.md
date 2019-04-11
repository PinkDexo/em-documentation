---
title: Changelog
taxonomy:
    category:
        - docs
---

#### v1.3.4 (April 12, 2019)

- Update: Drupal core to 8.6.14 for new installs.
- Update: Modules to the latest versions.
- Update: Font Awesome library to v5.8.1.
- New: Added page--node--panelized.html.twig template file. This template will override the default page template on all panelized nodes.
- Fix: Minor CSS fixes.
- Downgrade ctools, and panels module since this issue: https://www.drupal.org/project/panelizer/issues/3034080. If you like to use the latest versions of those modules, please consider applying patch #4 to Panelizer module. 

#### v1.3.3 (March 18, 2019)

- Update: Drupal core to 8.6.12 for new installs.
- Update: Modules to the latest versions.
- Fix: Call to a member function getExtension() when you use the base theme as a default theme.
- Fix: Panels and Panelizer modules are patched according to these issues: [Change panels store](https://www.drupal.org/project/panels/issues/3031778), [Change panelizer store](https://www.drupal.org/project/panelizer/issues/3034080).

#### v1.3.2 (March 4, 2019)

- Update: Drupal core to 8.6.10 for new installs
- Update: Modules to the latest versions
- Fix: A security fix in Drupal 8.6.10 prevents demo import.
- Fix: Notice: Undefined index: base_path in em_preprocess()

#### v1.3.1 (January 23, 2019)

- New: Added support for composer-managed Drupal projects with ready-made composer.json
- New: Added support for composer-managed Thunder projects with ready-made composer.json
- Update: Installation instructions for composer-managed sites.
- Update: Drupal core to 8.6.7 for new installs
- Update: Modules to the latest versions
- Fix: Incorrect path to logo image on a multilingual site.
- Fix: Social icons in the footer are not aligned at center


#### v1.3.0 (November 4, 2018)

- Added support for Poll module.
- Added support for MailChimp module.
- Added 3 Featured Grid layouts.
- Added 3 new Homepage Layouts.
- Added 6 new regions on the Homepage layout.
- Added Bootstrap responsive variation to grid layouts.
- Removed dependency for Twig Field Value and Twig Tweak module.
- Drupal Commerce is removed for new installs to simplify the maintenance of non commerce Drupal sites.
- Updated Bootstrap library to v4.1.3.
- Updated Documentation 
- New [Demo Page](https://em.pinkdexo.com/)

#### v1.2.2 (October 14, 2018)

- Fixed few JavaScript issues 
- Improved CSS for IE
- Improved IE 11 compatibility
- Bootstrap updated to version 4.1.3
- Font Awesome library updated to version 5.4 and now loading from CDN
- Modules updated to the latest version

#### v1.2.1 (October 5, 2018)

- Drupal updated to 8.6.1
- Modules updated to the latest version

#### v1.2.0 (July 12, 2018)

- Thunder Compatibility
- Improvement: Improved template files and styles to ensure the Thunder compatibility.
- Documentation: Added [instructions for installing](/using-with-thunder) EM theme and features on a Thunder distribution.

#### v1.1.0 (July 5, 2018)

- New Feature: Added Mega Menu.
- New Feature: Added Sticky header functionality.
- New Feature: Color module integration. Now the theme colors can be changed using Color module UI.
- Improvement: The template files for the Teasers are rewrite from the scratch to provide easy theme customization.
- Improvement: Added template for Error pages (403 & 404).
- Improvement: Added template for Maintenance page.
- Improvement: Added LinkedIn in the header's social media pages menu.
- Improvement: The uppercase on the headlines is removed.
- Fix: Social media links/icons on the author's page remains visible even if the link field is empty.
- Update: Bootstrap updated to v4.1.1.
- Update: Drupal core and Modules updated to the latest version.


#### v1.0.0 (April 11, 2018)

- Initial Release