# CP Sortable Custom Columns v. 1.1.2 for Craft CMS ![Craft 2.5](https://img.shields.io/badge/craft-2.5-red.svg?style=flat-square)

_Easily sort your element index tables on custom fields_

![Sorting on custom fields, like a champ](http://g.recordit.co/lhvfkHZj7E.gif)

## What?

The Customizable Element Index (CEI) feature in Craft 2.5+ lets users show or hide any custom field and/or metadata to the element indexes (i.e. the table listing your Entries, Categories, Assets or Users). Awesome stuff! Unfortunately though, Craft won't actually let you _sort_ elements on the columns you add – unless you add also add corresponding values to the sortable attributes in a custom plugin. Even then, there are issues, such as the sort menu not being _source aware_ (meaning all custom, sortable attributes added via the `modifyEntrySortableAttributes` hook will display for _all_ Sections), custom columns' headers are not clickable etc.

CP Sortable Custom Columns is a tiny plugin with a heavy handed name, aiming to hotfix the above issues.

## Features

* Automatically include any (sortable) custom field or meta value added to an element index in the sort menu
* Works with attributes added via the CEI interface or in plugin hooks (such as `defineAdditionalEntryTableAttributes`)
* Makes the headers for custom, sortable columns clickable, for easy sorting
* Makes the sorting menu _source aware_ – any column not in the current source's element index table will be removed from the sorting menu

With this plugin installed, any (sortable) custom field or meta value you add to an element index (either via hooks in a plugin, or via the CEI interface) will automatically be available for sorting.

## So which FieldTypes are sortable?

Any FieldType (custom or built-in) of the following [attribute types](https://craftcms.com/docs/plugins/field-types#customizing-the-database-column-type) are sortable:

* Number
* Date/Time
* String
* Boolean

Additionally, CP Sortable Custom Columns adds support for sorting on pretty much any meta field, such as Entry Type, Author, Updated Date etc.

## Requirements

CP Sortable Custom Columns requires Craft 2.5 or newer.

## Installation

* Download and unzip
* Move the `/cpsortcols` folder to your `/craft/plugins` folder
* Install from the Control Panel (`/admin/settings/plugins`)

## Disclaimer, bugs, feature request, support etc.

This plugin is provided free of charge and you can do whatever you want with it. CP Sortable Custom Columns is unlikely to mess up your stuff, but just to be clear: the author is not responsible for data loss or any other problems resulting from the use of this plugin.

Please report any bugs, feature requests or other issues [here](https://github.com/mmikkel/CpSortableCustomColumns/issues). Note that this is a hobby project and no promises are made regarding response time, feature implementations or bug fixes.

**Pull requests are extremely welcome**

### Changelog

#### 1.1.2 (06.26.2017)

* [Fixed] Fixes issue where CP Sortable Custom Columns would leak configuration data on login screen
* [Fixed] Fixes issue w/ sorting in Commerce active/inactive carts view (thanks @engram-design)

#### 1.1.1 (06.17.2016)

* [Fixed] Now works like it should for User element indexes.

#### 1.1 (02.24.2016)

* [Added] Adds support for Commerce Orders and Products (thanks Marion Newlevant!)

#### 1.0.2 (02.08.2016)

* [Fixed] Fixes an issue with Entry Type sorting
* [Improved] Now displays loading spinners for custom columns

#### 1.0.1 (01.31.2016)

* Fixes an issue with deactivated/uninstalled FieldTypes (thanks @carlcs, you're a champ!)

#### 1.0.0 (01.31.2016)

* Initial public release
