Повертає тип даних поля

-   [« odbc\_field\_scale](function.odbc-field-scale.html)
    
-   [odbc\_foreignkeys »](function.odbc-foreignkeys.html)
    
-   [PHP Manual](index.html)
    
-   [Функции ODBC](ref.uodbc.html)
    
-   Повертає тип даних поля
    

# odbcfieldtype

(PHP 4, PHP 5, PHP 7, PHP 8)

odbcfieldtype — Повертає тип даних поля

### Опис

```methodsynopsis
odbc_field_type(resource $statement, int $field): string|false
```

Отримує SQL тип поля, на яке посилається число в заданому ідентифікаторі результату.

### Список параметрів

`statement`

Ідентифікатор результату.

`field`

Номер поля. Нумерація полів починається з першого.

### Значення, що повертаються

Повертає тип поля у вигляді рядка або **`false`** у разі виникнення помилки.