---
navigation:
  - function.rrd-info.md: « rrd\_info
  - function.rrd-lastupdate.md: rrd\_lastupdate »
  - index.md: PHP Manual
  - ref.rrd.md: Функції RRD
title: rrd\_last
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# rrd\_last

(PECL rrd >= 0.9.0)

rrd\_last — Повертає позначку часу unix останнього зразка

### Опис

```methodsynopsis
rrd_last(string $filename): int
```

Повертає позначку часу UNIX останнього оновлення бази даних RRD.

### Список параметрів

`filename`

Назва файлу бази даних RRD.

### Значення, що повертаються

Ціле число, що представляє позначку часу unix останніх даних з бази даних RRD.
