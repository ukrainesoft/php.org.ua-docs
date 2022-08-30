Повертає кількість рядків, на які вплинув попередній запит

-   [« ibaseadduser](function.ibase-add-user.html)
    
-   [ibasebackup »](function.ibase-backup.html)
    
-   [PHP Manual](index.html)
    
-   [Функции Firebird/InterBase](ref.ibase.html)
    
-   Повертає кількість рядків, на які вплинув попередній запит
    

# ibaseaffectedrows

(PHP 5, PHP 7 < 7.4.0)

ibaseaffectedrows — Повертає кількість рядків, на які вплинув попередній запит

### Опис

```methodsynopsis
ibase_affected_rows(resource $link_identifier = ?): int
```

Ця функція повертає кількість рядків, на які вплинув попередній запит (INSERT, UPDATE або DELETE), виконаний із зазначеного контексту транзакції.

### Список параметрів

`link_identifier`

Контекст транзакції. Якщо `link_identifier` є ресурсом з'єднання, використовується його транзакція за умовчанням.

### Значення, що повертаються

Повертає кількість рядків як цілого числа.

### Дивіться також

-   [ibasequery()](function.ibase-query.html) - Виконує запит до бази даних InterBase
-   [ibaseexecute()](function.ibase-execute.html) - Виконує попередньо підготовлений запит