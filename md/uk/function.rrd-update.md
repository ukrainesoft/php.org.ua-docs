---
navigation:
  - function.rrd-tune.md: « rrd\_tune
  - function.rrd-version.md: rrd\_version »
  - index.md: PHP Manual
  - ref.rrd.md: Функції RRD
title: rrd\_update
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# rrd\_update

(PECL rrd >= 0.9.0)

rrd\_update — Оновлює базу даних RRD

### Опис

```methodsynopsis
rrd_update(string $filename, array $options): bool
```

Оновлює файл бази даних RRD. Вхідні дані - це час, інтерполіроване відповідно до властивостей файлу бази даних RRD.

### Список параметрів

`filename`

Назва файлу бази даних RRD. Ця база даних буде оновлена.

`options`

Опції поновлення бази даних RRD. Це перелік рядків. Повний список опцій дивіться на сторінці посібника з rrd update для отримання повного списку опцій.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.
