---
navigation:
  - function.rrd-version.md: « rrdversion
  - function.rrdc-disconnect.md: rrdcdisconnect »
  - index.md: PHP Manual
  - ref.rrd.md: Функції RRD
title: rrdxport
---
# rrdxport

(PECL rrd >= 0.9.0)

rrdxport — Експортує інформацію про базу даних RRD

### Опис

```methodsynopsis
rrd_xport(array $options): array
```

Експортує інформацію про файл бази даних RRD. Дані можуть бути перетворені в XML-файл за допомогою PHP-скрипта користувача, а потім відновлені у вигляді файлу бази даних RRD.

### Список параметрів

`options`

Масив опцій для експорту дивіться сторінку посібника з rrd xport.

### Значення, що повертаються

Масив з інформацією про файл бази даних RRD або **`false`** у разі виникнення помилки.
