---
navigation:
  - ref.rrd.md: « Функції RRD
  - function.rrd-error.md: rrd\_error »
  - index.md: PHP Manual
  - ref.rrd.md: Функції RRD
title: rrd\_create
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# rrd\_create

(PECL rrd >= 0.9.0)

rrd\_create — Створити файл rrd

### Опис

```methodsynopsis
rrd_create(string $filename, array $options): bool
```

Створює файл rrd.

### Список параметрів

`filename`

Ім'я файлу, що створюється.

`options`

Опції для створення rrd – список рядків. Дивіться сторінку посібника rrd для повного списку.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.
