Закриває об'єкт LOB

-   [« cubridlob2bind](function.cubrid-lob2-bind.html)
    
-   [cubridlob2export »](function.cubrid-lob2-export.html)
    
-   [PHP Manual](index.md)
    
-   [Функции CUBRID](ref.cubrid.md)
    
-   Закриває об'єкт LOB
    

# cubridlob2close

(PECL CUBRID >= 8.4.1)

cubridlob2close — Закриває об'єкт LOB

### Опис

```methodsynopsis
cubrid_lob2_close(resource $lob_identifier): bool
```

Функція **cubridlob2close()** використовується для закриття об'єкта LOB, повернутих функцією [cubridlob2new()](function.cubrid-lob2-new.html) або отриманого із результуючого набору.

### Список параметрів

`lob_identifier`

Ідентифікатор LOB, повернутий функцією [cubridlob2new()](function.cubrid-lob2-new.html) або отриманий із результуючого набору.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Дивіться також

-   [cubridlob2new()](function.cubrid-lob2-new.html) - Створює об'єкт LOB