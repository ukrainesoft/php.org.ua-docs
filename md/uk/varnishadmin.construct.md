---
navigation:
  - varnishadmin.connect.md: '« VarnishAdmin::connect'
  - varnishadmin.disconnect.md: 'VarnishAdmin::disconnect »'
  - index.md: PHP Manual
  - class.varnishadmin.md: VarnishAdmin
title: 'VarnishAdmin::\_\_construct'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# VarnishAdmin::\_\_construct

(PECL varnish >= 0.3)

VarnishAdmin::\_\_construct — VarnishAdmin constructor

### Опис

```methodsynopsis
public VarnishAdmin::__construct(array $args = ?)
```

### Список параметрів

`args`

Аргументи конфігурації. Можливі ключі:

VARNISH\_CONFIG\_IDENT - ідентифікатор екземпляра varnish VARNISH\_CONFIG\_HOST - IP-адреса екземпляра varnish VARNISH\_CONFIG\_PORT - порт екземпляра varnish VARNISH\_CONFIG\_SECRET - секрет екземпляра varnish VARNISH\_CONFIG\_TIMEOUT – час очікування читання підключення VARNISH\_CONFIG\_COMPAT - сумісність із старшими версіями varnish

### Значення, що повертаються

### Приклади

**Пример #1 Пример использования**VarnishAdmin::\_\_construct()\*\*\*\*

```php
<?php
    $args = array(
        VARNISH_CONFIG_HOST => "::1",
        VARNISH_CONFIG_PORT => 6082,
        VARNISH_CONFIG_SECRET => "5174826b-8595-4958-aa7a-0609632ad7ca",
        VARNISH_CONFIG_TIMEOUT => 300,
    );
    $va = new VarnishAdmin($args);
?>
```
