Просте використання VarnishLog

-   [« Простое использование VarnishStat](varnish.example.stat.md)
    
-   [VarnishAdmin »](class.varnishadmin.md)
    
-   [PHP Manual](index.md)
    
-   [Приклади](varnish.examples.md)
    
-   Просте використання VarnishLog
    

## Просте використання VarnishLog

Даний приклад ілюструє читання рядків журналу varnish з пам'яті, що розділяється

**Приклад #1 Прочитати журнал пам'яті varnish**

```php
<?php

$vl = new VarnishLog;
while(1) {
    $line = $vl->getLine();
    printf("%s %d %s", VarnishLog::getTagName($line['tag']), $line['id'],
    $line['data']);
}

exit(0);
?>
```