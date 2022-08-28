Встановлює час очікування на виконання запиту

-   [« cubrid\_set\_drop](function.cubrid-set-drop.html)
    
-   [cubrid\_version »](function.cubrid-version.html)
    
-   [PHP Manual](index.html)
    
-   [Функции CUBRID](ref.cubrid.html)
    
-   Встановлює час очікування на виконання запиту
    

# cubridsetquerytimeout

(PECL CUBRID >= 8.4.1)

cubridsetquerytimeout — Встановлює час очікування на виконання запиту

### Опис

```methodsynopsis
cubrid_set_query_timeout(resource $req_identifier, int $timeout): bool
```

Функція **cubridsetquerytimeout()** використовується для встановлення часу очікування на виконання запиту.

### Список параметрів

`req_identifier`

Request identifier.

`timeout`

Час очікування в мілісекундах.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Дивіться також

-   [cubrid\_get\_query\_timeout()](function.cubrid-get-query-timeout.html) - Отримує значення часу очікування запиту