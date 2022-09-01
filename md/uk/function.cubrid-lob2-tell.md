---
navigation:
  - function.cubrid-lob2-tell64.html: « cubridlob2tell64
  - function.cubrid-lob2-write.html: cubridlob2write »
  - index.md: PHP Manual
  - ref.cubrid.md: Функции CUBRID
title: cubridlob2tell
---
# cubridlob2tell

(PECL CUBRID >= 8.4.1)

cubridlob2tell - Повідомляє положення курсора LOB-об'єкта

### Опис

```methodsynopsis
cubrid_lob2_tell(resource $lob_identifier): int
```

Функція **cubridlob2tell()** використовується визначення положення курсора LOB-объекта.

### Список параметрів

`lob_identifier`

Ідентифікатор Lob в результаті [cubridlob2new()](function.cubrid-lob2-new.md) або отриманий із набору результатів.

### Значення, що повертаються

Повертає позицію курсора LOB-об'єкта, коли він буде успішно оброблений або **`false`** у разі виникнення помилки.

### Дивіться також

-   [cubridlob2read()](function.cubrid-lob2-read.md) - Здійснює читання з даних BLOB/CLOB
-   [cubridlob2write()](function.cubrid-lob2-write.md) - Записує до LOB-об'єкту
-   [cubridlob2seek()](function.cubrid-lob2-seek.md) - Переміщує курсор LOB-об'єкта
-   [cubridlob2seek64()](function.cubrid-lob2-seek64.md) - Переміщує курсор LOB-об'єкта
-   [cubridlob2tell64()](function.cubrid-lob2-tell64.md) - Повідомляє положення курсору LOB-об'єкта
-   [cubridlob2size()](function.cubrid-lob2-size.md) - Отримує розмір LOB-об'єкта
-   [cubridlob2size64()](function.cubrid-lob2-size64.md) - Отримує розмір LOB-об'єкта
