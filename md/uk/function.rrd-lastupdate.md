---
navigation:
  - function.rrd-last.md: « rrd\_last
  - function.rrd-restore.md: rrd\_restore »
  - index.md: PHP Manual
  - ref.rrd.md: Функції RRD
title: rrd\_lastupdate
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# rrd\_lastupdate

(PECL rrd >= 0.9.0)

rrd\_lastupdate — Отримує інформацію про останні оновлені дані

### Опис

```methodsynopsis
rrd_lastupdate(string $filename): array
```

Повертає масив позначки часу UNIX та значення, збережені для кожної дати в останньому оновленні файлу бази даних RRD.

### Список параметрів

`file`

Назва файлу бази даних RRD.

### Значення, що повертаються

Массив информации о последнем обновлении или\*\*`false`\*\*в случае возникновения ошибки.
