---
navigation:
  - function.rrd-restore.md: « rrd\_restore
  - function.rrd-update.md: rrd\_update »
  - index.md: PHP Manual
  - ref.rrd.md: Функції RRD
title: rrd\_tune
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# rrd\_tune

(PECL rrd >= 0.9.0)

rrd\_tune — Налаштовує деякі опції заголовка файлу бази даних RRD

### Опис

```methodsynopsis
rrd_tune(string $filename, array $options): bool
```

Змінити деякі опції файлу заголовка бази даних RRD. Наприклад, перейменовує джерело даних тощо.

### Список параметрів

`filename`

Назва файлу бази даних RRD.

`options`

Опції із властивостями файлу бази даних RRD, які будуть змінені. Дивіться сторінку посібника з rrd tune для подробиць.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.
