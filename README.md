# WP BootWalker

WordPress Nav Walker to implement multilevel Bootstrap 4.0.0-beta navbars.

* * *

## Requirements

* PHP 5.4+
* WordPress 4.4+

## Installation

Easy installation with [Composer](https://getcomposer.org/).

````
composer require bccampus/wp-bootwalker
````

## Usage (Bootstrap 4)

Update `wp_nav_menu()` to use the `BCcampus\BootWalker` walker. For example:

```
<?php

wp_nav_menu([
    'theme_location' => 'primary_navigation',
    'menu' => 'Primary Navigation',
    'depth' => 3,
    'container' => 'div',
    'container_class' => 'collapse navbar-collapse',
    'container_id' => 'navbarNav',
    'menu_class' => 'navbar-nav mr-auto',
    'fallback_cb' => '__return_empty_string',
    'walker' => new \BCcampus\BootWalker()
]);
```
[Bootstrap Navbar Documentation](https://getbootstrap.com/docs/4.0/components/navbar/)


## Additional CSS

You will want to modify the look and feel of the tier 3 'submenu'. Something like this will get you started.

```
.submenu{
  background-color: grey;
  padding-left: 1.70rem;
  a{
    font-size: smaller;
  }
}
```

## License

This has been modified from the [original](https://github.com/indigotree/wp-bootstrap-nav-walker) which is Copyright (c) 2017 Indigo Tree.
Modifications are Copyright &copy; Brad Payne and are released under the same MIT license.

The MIT [License](LICENSE.md) (MIT).
