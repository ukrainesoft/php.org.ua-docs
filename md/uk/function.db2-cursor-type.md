Повертає тип курсору, який використовується у ресурсі оператора

-   [« db2\_connect](function.db2-connect.html)
    
-   [db2\_escape\_string »](function.db2-escape-string.html)
    
-   [PHP Manual](index.html)
    
-   [Функции IBM DB2](ref.ibm-db2.html)
    
-   Повертає тип курсору, який використовується у ресурсі оператора
    

# db2cursortype

(PECL ibmdb2> = 1.0.0)

db2cursortype — Повертає тип курсору, який використовується у ресурсі оператора

### Опис

```methodsynopsis
db2_cursor_type(resource $stmt): int
```

Повертає тип курсору, який використовується у ресурсі оператора.

### Список параметрів

`stmt`

Коректний ресурс оператора.

### Значення, що повертаються

Повертає або `DB2_FORWARD_ONLY`, або `DB2_SCROLLABLE`, в залежності від типу курсора, що використовується.

### Дивіться також

-   [db2\_prepare()](function.db2-prepare.html) - готує SQL-запит до виконання