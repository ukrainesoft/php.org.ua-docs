---
navigation:
  - varnish.example.admin.html: « Простое использование VarnishAdmin
  - varnish.example.log.html: Простое использование VarnishLog »
  - index.html: PHP Manual
  - varnish.examples.html: Приклади
title: Просте використання VarnishStat
---
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
