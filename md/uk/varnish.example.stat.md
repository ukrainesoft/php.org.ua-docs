Просте використання VarnishStat

-   [« Простое использование VarnishAdmin](varnish.example.admin.html)
    
-   [Простое использование VarnishLog »](varnish.example.log.html)
    
-   [PHP Manual](index.html)
    
-   [Приклади](varnish.examples.html)
    
-   Просте використання VarnishStat
    

## Просте використання VarnishStat

Даний приклад ілюструє отримання знімка статистики varnish з пам'яті, що розділяється

**Приклад #1 Отримати фотографію статистики**

```php
<?php

$vs = new VarnishStat;

try {
    $data = $vs->getSnapshot();
} catch (VarnishException $e) {
    echo $e->getMessage();
    exit(3);
}

exit(0);
?>
```