---
navigation:
  - varnishadmin.ban.md: '« VarnishAdmin::ban'
  - varnishadmin.clearpanic.md: 'VarnishAdmin::clearPanic »'
  - index.md: PHP Manual
  - class.varnishadmin.md: VarnishAdmin
title: 'VarnishAdmin::banUrl'
---
# VarnishAdmin::banUrl

(PECL varnish >= 0.3)

VarnishAdmin::banUrl — Заборонити URL-адресу, використовуючи вираз VCL

### Опис

```methodsynopsis
public VarnishAdmin::banUrl(string $vcl_regex): int
```

### Список параметрів

`vcl_regex`

Регулярний вираз URL у синтаксисі, сумісному з PCRE. Воно ґрунтується на команді varnish ban.

### Значення, що повертаються

Повертає статус команди Varnish.
