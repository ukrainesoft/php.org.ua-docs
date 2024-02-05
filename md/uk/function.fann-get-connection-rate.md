---
navigation:
  - function.fann-get-connection-array.md: « fann\_get\_connection\_array
  - function.fann-get-errno.md: fann\_get\_errno »
  - index.md: PHP Manual
  - ref.fann.md: Функції Fann
title: fann\_get\_connection\_rate
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# fann\_get\_connection\_rate

(PECL fann >= 1.0.0)

fann\_get\_connection\_rate — Отримує швидкість з'єднання, що використовується під час створення мережі

### Опис

```methodsynopsis
fann_get_connection_rate(resource $ann): float
```

Отримує швидкість з'єднання, що використовується під час створення мережі.

### Список параметрів

`ann`

Ресурс нейронної мережі.

### Значення, що повертаються

Швидкість з'єднання, використана при створенні мережі або \*\*`false`\*\*в случае возникновения ошибки.
