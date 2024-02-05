---
navigation:
  - varnishadmin.auth.md: '« VarnishAdmin::auth'
  - varnishadmin.banurl.md: 'VarnishAdmin::banUrl »'
  - index.md: PHP Manual
  - class.varnishadmin.md: VarnishAdmin
title: 'VarnishAdmin::ban'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# VarnishAdmin::ban

(PECL varnish >= 0.3)

VarnishAdmin::ban — Заборонити URL-адресу, використовуючи вираз VCL

### Опис

```methodsynopsis
public VarnishAdmin::ban(string $vcl_regex): int
```

### Список параметрів

`vcl_regex`

Вираз Varnish VCL. Воно ґрунтується на команді varnish ban.

### Значення, що повертаються

Повертає статус команди Varnish.
