---
navigation:
  - function.rrd-lastupdate.md: « rrdlastupdate
  - function.rrd-tune.md: rrdtune »
  - index.md: PHP Manual
  - ref.rrd.md: Функції RRD
title: rrdrestore
---
# rrdrestore

(PECL rrd >= 0.9.0)

rrdrestore — Відновлює RRD із дампи XML.

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

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.
