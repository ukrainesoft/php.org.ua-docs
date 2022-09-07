---
navigation:
  - varnish.example.admin.md: « Простое использование VarnishAdmin
  - varnish.example.log.md: Простое использование VarnishLog »
  - index.md: PHP Manual
  - varnish.examples.md: Приклади
title: Просте використання VarnishStat
---
## Просте використання VarnishStat

Даний приклад ілюструє отримання знімка статистики varnish з пам'яті, що розділяється

**Приклад #1 Отримати фотографію статистики**

```php
<?php

$vs = new VarnishStat;

try {
    $data = $vs->getSnapshot();
} catch (VarnishException $e) {
    echo $e->getMessage();
    exit(3);
}

exit(0);
?>
```
