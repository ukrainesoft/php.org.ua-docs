---
navigation:
  - function.rrd-last.html: « rrdlast
  - function.rrd-restore.html: rrdrestore »
  - index.md: PHP Manual
  - ref.rrd.md: Функції RRD
title: rrdlastupdate
---
# rrdlastupdate

(PECL rrd >= 0.9.0)

rrdlastupdate — Отримує інформацію про останні оновлені дані

### Опис

```methodsynopsis
rrd_lastupdate(string $filename): array
```

Повертає масив позначки часу UNIX та значення, збережені для кожної дати в останньому оновленні файлу бази даних RRD.

### Список параметрів

`file`

Назва файлу бази даних RRD.

### Значення, що повертаються

Масив інформації про останнє оновлення або **`false`** у разі виникнення помилки.
