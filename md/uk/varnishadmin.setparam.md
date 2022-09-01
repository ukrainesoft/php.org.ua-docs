---
navigation:
  - varnishadmin.setident.md: '« VarnishAdmin::setIdent'
  - varnishadmin.setport.md: 'VarnishAdmin::setPort »'
  - index.md: PHP Manual
  - class.varnishadmin.md: VarnishAdmin
title: 'VarnishAdmin::setParam'
---
# VarnishAdmin::setParam

(PECL varnish >= 0.4)

VarnishAdmin::setParam — Встановити параметр конфігурації на поточному екземплярі varnish

### Опис

```methodsynopsis
public VarnishAdmin::setParam(string $name, string|int $value): int
```

### Список параметрів

`name`

Назва параметра конфігурації Varnish.

`value`

Значення параметра конфігурації Varnish.

### Значення, що повертаються

Повертає статус команди Varnish.
