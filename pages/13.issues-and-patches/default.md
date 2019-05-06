---
title: 'Issues and Patches'
---

Patches are a common thing when you work with Drupal. They are pieces of code that describes the changes between a before and after state of either a module or core. We commonly use patches to improve the code, add extra functionalities to a module or fix an existing issue. By applying the patch, the issue should no longer exist.

This item uses a few contributed Drupal modules that need to be patched for the theme to work as is designed.  However, if you have purchased this item, you shouldn't worry about applying patches because the package includes already patched modules.

This document is for informational purposes only so that in the future if you update some of the modules below you should follow the module's issue, and you may need to [apply a patch](https://www.drupal.org/patch/apply) if the module maintainer does not have fixed the problem yet. If you use a composer managed version of the theme, you don't have to worry about applying patches. The patches are listed in the composer.json file, and they will be automatically applied when you perform an update on a patched module.


---

##### **Page Manager**

**issue**: [Incorrect page_title title in browser toolbar](https://www.drupal.org/project/page_manager/issues/2752227)<br>
**patch**: [#37 - page_manager-incorrect-page_title-2752227-37-8.x.4.x.patch](https://www.drupal.org/files/issues/2018-10-26/page_manager-incorrect-page_title-2752227-37-8.x.4.x.patch)

---

##### **Panels**

**issue**: [Page title does not display](https://www.drupal.org/project/panels/issues/2869412)<br>
**patch**: [#27 - panels--page_title_does_not_display--2869412-27.patch](https://www.drupal.org/files/issues/2018-03-19/panels--page_title_does_not_display--2869412-27.patch)

**issue**: [Changes to Layout not being saved](https://www.drupal.org/project/panels/issues/2824632)<br>
**patch**: [#16 - panels-fix_updating_layout-2824632-16-D8.patch](https://www.drupal.org/files/issues/2018-08-28/panels-fix_updating_layout-2824632-16-D8.patch)

---

##### **Poll**
issue: [Most Recent Poll - Question title is Displayed as Block Title](https://www.drupal.org/project/poll/issues/2923946)<br>
patch: [#7 - question-title-is-displayed-as-block-title-2923946-8.x-1.x-dev-7.patch](https://www.drupal.org/files/issues/2019-03-15/question-title-is-displayed-as-block-title-2923946-8.x-1.x-dev-7.patch)

---

##### **Mailchimp**
issue: [Notice: Undefined property: stdClass::$size in mailchimp_insert_drupal_form_tag()](https://www.drupal.org/project/mailchimp/issues/2936099)<br>
patch: [#6 - suppress-size-notice-2936099-6.patch](https://www.drupal.org/files/issues/2018-06-07/suppress-size-notice-2936099-6.patch)

---

### Updating Drupal and contributed modules

! When you plan to perform an update, please follow the Drupal's documentation on how to update the [core](https://www.drupal.org/docs/8/update) and [modules](https://www.drupal.org/docs/8/update/update-modules). You should consider that sometimes updates may break your website or some of its functionalities. A reason for this can be a bug in a module, conflict with some other modules or core, missing dependency or incompatibility with your environment. Breaking your site or functionalities with performing module updates or installing new modules **IS NOT AN ITEM ISSUE NOR A THEME ISSUE** and is not covered by the [ThemeForest support policy](https://themeforest.net/page/item_support_policy). 

If you find yourself in a situation like this from above, try to google the error thrown by your site or go to the module's [issue queue](https://www.drupal.org/docs/develop/for-gci-students-where-to-start/using-the-issue-queue) to find a fix or solutions for the problem. In case if you don't succeed in fixing the problem, revert the changes until you find a proper solution for your issue.

