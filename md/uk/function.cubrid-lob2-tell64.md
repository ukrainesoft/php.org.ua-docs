---
navigation:
  - function.cubrid-lob2-size.md: « cubrid\_lob2\_size
  - function.cubrid-lob2-tell.md: cubrid\_lob2\_tell »
  - index.md: PHP Manual
  - ref.cubrid.md: Функції CUBRID
title: cubrid\_lob2\_tell64
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# cubrid\_lob2\_tell64

(PECL CUBRID >= 8.4.1)

cubrid\_lob2\_tell64 - Повідомляє положення курсора LOB-об'єкта

### Опис

```methodsynopsis
cubrid_lob2_tell64(resource $lob_identifier): string
```

Функция**cubrid\_lob2\_tell64()** використовується визначення положення курсора LOB-объекта. Якщо розмір LOB-об'єкта більший, ніж можуть бути збережені цілі дані, ви можете використовувати цю функцію і вона поверне інформацію про позицію у вигляді рядка.

### Список параметрів

`lob_identifier`

Идентификатор Lob в результате[cubrid\_lob2\_new()](function.cubrid-lob2-new.md) або отриманий із набору результатів.

### Значення, що повертаються

Повертає позицію курсора LOB-об'єкта у вигляді рядка у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Дивіться також

-   [cubrid\_lob2\_read()](function.cubrid-lob2-read.md) \- Здійснює читання з даних BLOB/CLOB
-   [cubrid\_lob2\_write()](function.cubrid-lob2-write.md) \- Записує до LOB-об'єкту
-   [cubrid\_lob2\_seek()](function.cubrid-lob2-seek.md) \- Переміщує курсор LOB-об'єкта
-   [cubrid\_lob2\_seek64()](function.cubrid-lob2-seek64.md) \- Переміщує курсор LOB-об'єкта
-   [cubrid\_lob2\_tell()](function.cubrid-lob2-tell.md) \- Повідомляє положення курсору LOB-об'єкта
-   [cubrid\_lob2\_size()](function.cubrid-lob2-size.md) \- Отримує розмір LOB-об'єкта
-   [cubrid\_lob2\_size64()](function.cubrid-lob2-size64.md) \- Отримує розмір LOB-об'єкта
