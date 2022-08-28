Повертає ім'я стовпця

-   [« odbc\_field\_len](function.odbc-field-len.html)
    
-   [odbc\_field\_num »](function.odbc-field-num.html)
    
-   [PHP Manual](index.html)
    
-   [Функции ODBC](ref.uodbc.html)
    
-   Повертає ім'я стовпця
    

# odbcfieldname

(PHP 4, PHP 5, PHP 7, PHP 8)

odbcfieldname — Повертає ім'я стовпця

### Опис

```methodsynopsis
odbc_field_name(resource $statement, int $field): string|false
```

Повертає ім'я поля, що займає номер стовпця в заданому ідентифікаторі результату.

### Список параметрів

`statement`

Ідентифікатор результату.

`field`

Номер поля. Нумерація полів починається з першого.

### Значення, що повертаються

Повертає ім'я поля у вигляді рядка або **`false`** у разі виникнення помилки.