Повертає тип даних поля

-   [« odbcfieldscale](function.odbc-field-scale.html)
    
-   [odbcforeignkeys »](function.odbc-foreignkeys.html)
    
-   [PHP Manual](index.md)
    
-   [Функции ODBC](ref.uodbc.md)
    
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