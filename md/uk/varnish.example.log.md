---
navigation:
  - varnish.example.stat.md: « Просте використання VarnishStat
  - class.varnishadmin.md: VarnishAdmin »
  - index.md: PHP Manual
  - varnish.examples.md: Приклади
title: Просте використання VarnishLog
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
## Просте використання VarnishLog

Даний приклад ілюструє читання рядків журналу varnish з пам'яті, що розділяється

**Приклад #1 Прочитати журнал пам'яті varnish**

```php
<?php

$vl = new VarnishLog;
while(1) {
    $line = $vl->getLine();
    printf("%s %d %s", VarnishLog::getTagName($line['tag']), $line['id'],
    $line['data']);
}

exit(0);
?>
```
