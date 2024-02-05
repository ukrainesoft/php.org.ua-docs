---
navigation:
  - function.cubrid-lob2-size64.md: « cubrid\_lob2\_size64
  - function.cubrid-lob2-tell64.md: cubrid\_lob2\_tell64 »
  - index.md: PHP Manual
  - ref.cubrid.md: Функції CUBRID
title: cubrid\_lob2\_size
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# cubrid\_lob2\_size

(PECL CUBRID >= 8.4.1)

cubrid\_lob2\_size — Отримує розмір LOB-об'єкта

### Опис

```methodsynopsis
cubrid_lob2_size(resource $lob_identifier): int
```

Функция**cubrid\_lob2\_size()** використовується отримання розміру LOB-объекта.

### Список параметрів

`lob_identifier`

Ідентифікатор LOB внаслідок роботи функції [cubrid\_lob2\_new()](function.cubrid-lob2-new.md) або отриманий із набору результатів.

### Значення, що повертаються

Повертає розмір LOB-об'єкта у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Дивіться також

-   [cubrid\_lob2\_read()](function.cubrid-lob2-read.md) \- Здійснює читання з даних BLOB/CLOB
-   [cubrid\_lob2\_write()](function.cubrid-lob2-write.md) \- Записує до LOB-об'єкту
-   [cubrid\_lob2\_seek()](function.cubrid-lob2-seek.md) \- Переміщує курсор LOB-об'єкта
-   [cubrid\_lob2\_seek64()](function.cubrid-lob2-seek64.md) \- Переміщує курсор LOB-об'єкта
-   [cubrid\_lob2\_tell()](function.cubrid-lob2-tell.md) \- Повідомляє положення курсору LOB-об'єкта
-   [cubrid\_lob2\_tell64()](function.cubrid-lob2-tell64.md) \- Повідомляє положення курсору LOB-об'єкта
-   [cubrid\_lob2\_size64()](function.cubrid-lob2-size64.md) \- Отримує розмір LOB-об'єкта
