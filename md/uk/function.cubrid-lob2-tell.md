Повідомляє положення курсору LOB-об'єкта

-   [« cubridlob2tell64](function.cubrid-lob2-tell64.html)
    
-   [cubridlob2write »](function.cubrid-lob2-write.html)
    
-   [PHP Manual](index.md)
    
-   [Функции CUBRID](ref.cubrid.md)
    
-   Повідомляє положення курсору LOB-об'єкта
    

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

Ідентифікатор Lob в результаті [cubridlob2new()](function.cubrid-lob2-new.html) або отриманий із набору результатів.

### Значення, що повертаються

Повертає позицію курсора LOB-об'єкта, коли він буде успішно оброблений або **`false`** у разі виникнення помилки.

### Дивіться також

-   [cubridlob2read()](function.cubrid-lob2-read.html) - Здійснює читання з даних BLOB/CLOB
-   [cubridlob2write()](function.cubrid-lob2-write.html) - Записує до LOB-об'єкту
-   [cubridlob2seek()](function.cubrid-lob2-seek.html) - Переміщує курсор LOB-об'єкта
-   [cubridlob2seek64()](function.cubrid-lob2-seek64.html) - Переміщує курсор LOB-об'єкта
-   [cubridlob2tell64()](function.cubrid-lob2-tell64.html) - Повідомляє положення курсору LOB-об'єкта
-   [cubridlob2size()](function.cubrid-lob2-size.html) - Отримує розмір LOB-об'єкта
-   [cubridlob2size64()](function.cubrid-lob2-size64.html) - Отримує розмір LOB-об'єкта