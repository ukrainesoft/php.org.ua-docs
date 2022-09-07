---
navigation:
  - function.rrd-restore.md: « rrdrestore
  - function.rrd-update.md: rrdupdate »
  - index.md: PHP Manual
  - ref.rrd.md: Функції RRD
title: rrdtune
---
# rrdtune

(PECL rrd >= 0.9.0)

rrdtune — Налаштування деяких параметрів заголовка файлу бази даних RRD

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

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.
