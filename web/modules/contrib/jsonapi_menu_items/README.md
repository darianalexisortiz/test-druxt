# JSON API Menu items

[![CircleCI](https://circleci.com/gh/Realityloop/jsonapi_menu_items.svg?style=svg)](https://circleci.com/gh/Realityloop/jsonapi_menu_items)

> Adds a JSON API resource for menu items: `/jsonapi/menu_items/{menu}`


## Features

- Supports user and system created menu items.
- Supports `menu_link_content` and [menu_link_config](https://www.drupal.org/project/menu_link_config) menu items.
- Supports filtering by depth, parents and custom query conditions.
- Optional support for [JSON:API Hypermedia](https://www.drupal.org/project/jsonapi_hypermedia) based links in `/jsonapi` root document.


## Filters

- **min_depth**

  Sets the minimum depth of menu links in the resulting tree relative to the root.

  Example: `?filter[min_depth]=2`

- **max_depth**

  Sets the maximum depth of menu links in the resulting tree relative to the root.

  Example: `?filter[max_depth]=2`

- **parent**

  Sets a root for menu tree loading.

  Example: `?filter[parent]=system.admin`

- **parents**

  Adds parent menu links IDs to restrict the tree.

  Example: `?filter[parent]=system.admin,system.admin_structure`

- **conditions[]**

  Adds a custom query condition.

  Example: `?filter[conditions][provider][value]=system`
