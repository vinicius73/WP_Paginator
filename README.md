WP_Paginator
============

Pagination class for worpress

## Usage

```php
echo WP_Paginator::make();
## Params
$paginator = WP_Paginator::make(array $args = array(), $pages = null, $range = 2, $_wp_query = null);
// or 
$paginator = new WP_Paginator(array $args = array(), $pages = null, $range = 2, $_wp_query = null);

echo $paginator; //echo $paginator->render();
```

### Customization

You have a lot of freedom to customize the elements to be rendered  
By default pages are rendered with classes and elements of the Twitter Bootstrap

```php
$args = array(
        'before'      => '<ul class="pagination %1$s">',
        'after'       => '</ul>',
        'before_link' => '<li class="%1$s">',
        'after_link'  => '</li>',
        'link'        => '<a class="%3$s" href="%1$s">%2$s</a>',
        'class'       => array(
            'disabled' => 'disabled',
            'active'   => 'active',
            'before'   => null,
            'prev'     => null,
            'after'    => null,
            'first'    => null,
            'last'     => null,
            'back'     => null,
            'next'     => null,
            'link'     => null
        ),
        'labels'      => array(
            'first'  => 'first',
            'last'   => 'last',
            'prev'   => '&laquo;',
            'next'   => '&raquo;',
            'active' => '%1$s <span class="sr-only">(current)</span>'
        )
    )
    
echo WP_Paginator::make($args);
```


## Credits
- Author - [Vinicius73](https://github.com/vinicius73)
