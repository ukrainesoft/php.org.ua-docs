Повертає довжину (точність) поля

-   [« odbc\_fetch\_row](function.odbc-fetch-row.html)
    
-   [odbc\_field\_name »](function.odbc-field-name.html)
    
-   [PHP Manual](index.html)
    
-   [Функции ODBC](ref.uodbc.html)
    
-   Повертає довжину (точність) поля
    

# odbcfieldlen

(PHP 4, PHP 5, PHP 7, PHP 8)

odbcfieldlen — Повертає довжину (точність) поля

### Опис

```methodsynopsis
odbc_field_len(resource $statement, int $field): int|false
```

Повертає довжину поля, на яке посилається число у заданому ідентифікаторі результату.

### Список параметрів

`statement`

Ідентифікатор результату.

`field`

Номер поля. Нумерація полів починається з першого.

### Значення, що повертаються

Повертає довжину поля або **`false`** у разі виникнення помилки.

### Дивіться також

-   [odbc\_field\_scale()](function.odbc-field-scale.html) - Повертає масштаб поля для набуття масштабу числа з плаваючою точкою