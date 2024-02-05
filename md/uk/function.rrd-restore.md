---
navigation:
  - function.rrd-lastupdate.md: « rrd\_lastupdate
  - function.rrd-tune.md: rrd\_tune »
  - index.md: PHP Manual
  - ref.rrd.md: Функції RRD
title: rrd\_restore
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# rrd\_restore

(PECL rrd >= 0.9.0)

rrd\_restore — Відновлює файл RRD із дампи XML

### Опис

```methodsynopsis
rrd_restore(string $xml_file, string $rrd_file, array $options = ?): bool
```

Відновлює файл RRD із дампи XML.

### Список параметрів

`xml_file`

Ім'я файлу XML із дампом вихідного файлу бази даних RRD.

`rrd_file`

Відновлена ​​назва файлу бази даних RRD.

`options`

Масив опцій для відновлення. Дивіться сторінку посібника з rrd restore.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.
