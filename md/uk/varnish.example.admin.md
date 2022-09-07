---
navigation:
  - varnish.examples.md: « Приклади
  - varnish.example.stat.md: Простое использование VarnishStat »
  - index.md: PHP Manual
  - varnish.examples.md: Приклади
title: Просте використання VarnishAdmin
---
## Просте використання VarnishAdmin

Цей приклад ілюструє просте використання функціональності заборони

**Приклад #1 Заборонити URL**

```php
<?php

$args = array(
    VARNISH_CONFIG_HOST    => "::1",
    VARNISH_CONFIG_PORT    => 6082,
    VARNISH_CONFIG_SECRET  => "5174826b-8595-4958-aa7a-0609632ad7ca",
    VARNISH_CONFIG_TIMEOUT => 300,
);

$va = new VarnishAdmin($args);

try {
    if(!$va->connect()) {
        throw new VarnishException("Неудачное подключение\n");
    }
} catch (VarnishException $e) {
    echo $e->getMessage();
    exit(3);
}

try {
    if(!$va->auth()) {
        throw new VarnishException("Неудачная аутентификация\n");
    }
} catch (VarnishException $e) {
    echo $e->getMessage();
    exit(3);
}

try {
    $status = $va->ban('req.url ~ "^/$"');
    if (VARNISH_STATUS_OK != $status) {
        throw new VarnishException("Метод ban вернул статус $status\n");
    }
} catch (VarnishException $e) {
    echo $e->getMessage();
    exit(3);
}

exit(0);

?>
```
