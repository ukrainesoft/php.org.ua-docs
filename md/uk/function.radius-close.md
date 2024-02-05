---
navigation:
  - function.radius-auth-open.md: « radius\_auth\_open
  - function.radius-config.md: radius\_config »
  - index.md: PHP Manual
  - ref.radius.md: Функції Radius
title: radius\_close
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# radius\_close

(PECL radius >= 1.1.0)

radius\_close - Звільняє всі ресурси

### Опис

```methodsynopsis
radius_close(resource $radius_handle): bool
```

Не потрібно викликати цю функцію, тому що PHP звільняє всі ресурси в кінці кожного запиту.

### Список параметрів

`radius_handle`

Ресурс RADIUS

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.
