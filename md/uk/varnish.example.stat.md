---
navigation:
  - varnish.example.admin.md: « Просте використання VarnishAdmin
  - varnish.example.log.md: Просте використання VarnishLog »
  - index.md: PHP Manual
  - varnish.examples.md: Приклади
title: Просте використання VarnishStat
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
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
