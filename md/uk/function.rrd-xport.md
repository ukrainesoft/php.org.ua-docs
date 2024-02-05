---
navigation:
  - function.rrd-version.md: « rrd\_version
  - function.rrdc-disconnect.md: rrdc\_disconnect »
  - index.md: PHP Manual
  - ref.rrd.md: Функції RRD
title: rrd\_xport
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# rrd\_xport

(PECL rrd >= 0.9.0)

rrd\_xport — Експортує інформацію про базу даних RRD

### Опис

```methodsynopsis
rrd_xport(array $options): array
```

Експортує інформацію про файл бази даних RRD. Дані можуть бути перетворені в XML-файл за допомогою PHP-скрипта користувача, а потім відновлені у вигляді файлу бази даних RRD.

### Список параметрів

`options`

Масив опцій для експорту дивіться сторінку посібника з rrd xport.

### Значення, що повертаються

Масив з інформацією про файл бази даних RRD або \*\*`false`\*\*в случае возникновения ошибки.
