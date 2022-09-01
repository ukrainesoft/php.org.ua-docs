---
navigation:
  - function.rrd-info.html: « rrdinfo
  - function.rrd-lastupdate.html: rrdlastupdate »
  - index.html: PHP Manual
  - ref.rrd.html: Функції RRD
title: rrdlast
---
# rrdlast

(PECL rrd >= 0.9.0)

rrdlast — Повертає позначку часу unix останнього зразка

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
