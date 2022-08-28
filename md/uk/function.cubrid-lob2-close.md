Закриває об'єкт LOB

-   [« cubrid\_lob2\_bind](function.cubrid-lob2-bind.html)
    
-   [cubrid\_lob2\_export »](function.cubrid-lob2-export.html)
    
-   [PHP Manual](index.html)
    
-   [Функции CUBRID](ref.cubrid.html)
    
-   Закриває об'єкт LOB
    

# cubridlob2close

(PECL CUBRID >= 8.4.1)

cubridlob2close — Закриває об'єкт LOB

### Опис

```methodsynopsis
cubrid_lob2_close(resource $lob_identifier): bool
```

Функція **cubridlob2close()** використовується для закриття об'єкта LOB, повернутих функцією [cubrid\_lob2\_new()](function.cubrid-lob2-new.html) або отриманого із результуючого набору.

### Список параметрів

`lob_identifier`

Ідентифікатор LOB, повернутий функцією [cubrid\_lob2\_new()](function.cubrid-lob2-new.html) або отриманий із результуючого набору.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Дивіться також

-   [cubrid\_lob2\_new()](function.cubrid-lob2-new.html) - Створює об'єкт LOB