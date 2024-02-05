---
navigation:
  - function.cubrid-lob2-bind.md: « cubrid\_lob2\_bind
  - function.cubrid-lob2-export.md: cubrid\_lob2\_export »
  - index.md: PHP Manual
  - ref.cubrid.md: Функції CUBRID
title: cubrid\_lob2\_close
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# cubrid\_lob2\_close

(PECL CUBRID >= 8.4.1)

cubrid\_lob2\_close — Закриває об'єкт LOB

### Опис

```methodsynopsis
cubrid_lob2_close(resource $lob_identifier): bool
```

Функция**cubrid\_lob2\_close()** використовується для закриття об'єкта LOB, повернутих функцією [cubrid\_lob2\_new()](function.cubrid-lob2-new.md)или полученного из результирующего набора.

### Список параметрів

`lob_identifier`

Ідентифікатор LOB, повернутий функцією [cubrid\_lob2\_new()](function.cubrid-lob2-new.md) або отриманий із результуючого набору.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Дивіться також

-   [cubrid\_lob2\_new()](function.cubrid-lob2-new.md) \- Створює об'єкт LOB
