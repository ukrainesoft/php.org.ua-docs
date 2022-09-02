---
navigation:
  - varnishadmin.connect.md: '« VarnishAdmin::connect'
  - varnishadmin.disconnect.md: 'VarnishAdmin::disconnect »'
  - index.md: PHP Manual
  - class.varnishadmin.md: VarnishAdmin
title: 'VarnishAdmin::construct'
---
# VarnishAdmin::construct

(PECL varnish >= 0.3)

VarnishAdmin::construct — VarnishAdmin constructor

### Опис

```methodsynopsis
public VarnishAdmin::__construct(array $args = ?)
```

### Список параметрів

`args`

Аргументи конфігурації. Можливі ключі:

VARNISHCONFIGIDENT - ідентифікатор екземпляра varnish VARNISHCONFIGHOST - IP-адреса екземпляра varnish VARNISHCONFIGPORT - порт екземпляра varnish VARNISHCONFIGSECRET - секрет екземпляра varnish VARNISHCONFIGTIMEOUT – час очікування читання підключення VARNISHCONFIGCOMPAT - сумісність із старшими версіями varnish

### Значення, що повертаються

### Приклади

**Приклад #1 Приклад використання **VarnishAdmin::construct()****

```php
<?php
    $args = array(
        VARNISH_CONFIG_HOST => "::1",
        VARNISH_CONFIG_PORT => 6082,
        VARNISH_CONFIG_SECRET => "5174826b-8595-4958-aa7a-0609632ad7ca",
        VARNISH_CONFIG_TIMEOUT => 300,
    );
    $va = new VarnishAdmin($args);
?>
```
