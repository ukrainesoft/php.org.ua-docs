Отримує значення часу очікування запиту

-   [« cubrid\_get\_db\_parameter](function.cubrid-get-db-parameter.html)
    
-   [cubrid\_get\_server\_info »](function.cubrid-get-server-info.html)
    
-   [PHP Manual](index.html)
    
-   [Функции CUBRID](ref.cubrid.html)
    
-   Отримує значення часу очікування запиту
    

# cubridgetquerytimeout

(PECL CUBRID >= 8.4.1)

cubridgetquerytimeout — Отримує значення часу очікування запиту

### Опис

```methodsynopsis
cubrid_get_query_timeout(resource $req_identifier): int
```

Функція **cubridgetquerytimeout()** використовується для отримання часу очікування.

### Список параметрів

`req_identifier`

Ідентифікатор запиту.

### Значення, що повертаються

Повертає значення часу очікування поточного запиту у мілісекундах у разі успішного виконання або **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання **cubridgetquerytimeout()****

```php
<?php

$host = "localhost";
$port = 33000;
$db = "demodb";

$conn =
cubrid_connect_with_url("CUBRID:$host:$port:$db:::?login_timeout=50000&query_timeout=5000&disconnect_on_query_timeout=yes");

$req = cubrid_prepare($conn, "SELECT * FROM code");

$timeout = cubrid_get_query_timeout($req);
var_dump($timeout);

cubrid_set_query_timeout($req, 1000);
$timeout = cubrid_get_query_timeout($req);
var_dump($timeout);

cubrid_close($conn);
?>
```

Результат виконання цього прикладу:

```
int(5000)
int(1000)
```

### Дивіться також

-   [cubrid\_set\_query\_timeout()](function.cubrid-set-query-timeout.html) - Встановлює час очікування на виконання запиту