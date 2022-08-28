Повертає номер стовпця

-   [« odbc\_field\_name](function.odbc-field-name.html)
    
-   [odbc\_field\_precision »](function.odbc-field-precision.html)
    
-   [PHP Manual](index.html)
    
-   [Функции ODBC](ref.uodbc.html)
    
-   Повертає номер стовпця
    

# odbcfieldnum

(PHP 4, PHP 5, PHP 7, PHP 8)

odbcfieldnum — Повертає номер стовпця

### Опис

```methodsynopsis
odbc_field_num(resource $statement, string $field): int|false
```

Отримує номер слота стовпця, який відповідає полю в заданому ідентифікаторі результату.

### Список параметрів

`statement`

Ідентифікатор результату.

`field`

Ім'я поля.

### Значення, що повертаються

Повертає номер поля у вигляді цілого чи числа **`false`** у разі виникнення помилки. Нумерація полів починається з першого.