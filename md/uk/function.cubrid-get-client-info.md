Повертає версію клієнтської бібліотеки

-   [« cubridgetclassname](function.cubrid-get-class-name.html)
    
-   [cubridgetдбparameter »](function.cubrid-get-db-parameter.html)
    
-   [PHP Manual](index.html)
    
-   [Функции CUBRID](ref.cubrid.html)
    
-   Повертає версію клієнтської бібліотеки
    

# cubridgetclientinfo

(PECL CUBRID >= 8.3.0)

cubridgetclientinfo — Повертає версію клієнтської бібліотеки

### Опис

```methodsynopsis
cubrid_get_client_info(): string
```

Функція повертає рядок, який представляє версію клієнтської бібліотеки.

### Список параметрів

### Значення, що повертаються

Рядок, що представляє версію клієнтської бібліотеки у разі успішного виконання або **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання **cubridgetclientinfo()****

```php
<?php
printf("%-30s %s\n", "Версия CUBRID PHP:", cubrid_version());

printf("\n");

$conn = cubrid_connect("localhost", 33088, "demodb");

if (!$conn) {
    die('Ошибка подключения ('. cubrid_error_code() .')' . cubrid_error_msg());
}

$db_params = cubrid_get_db_parameter($conn);

while (list($param_name, $param_value) = each($db_params)) {
    printf("%-30s %s\n", $param_name, $param_value);
}

printf("\n");

$server_info = cubrid_get_server_info($conn);
$client_info = cubrid_get_client_info();

printf("%-30s %s\n", "Информация о сервере:", $server_info);
printf("%-30s %s\n", "Информация о клиенте:", $client_info);

printf("\n");

$charset = cubrid_get_charset($conn);

printf("%-30s %s\n", "Кодировка CUBRID:", $charset);

cubrid_disconnect($conn);

?>
```

Результат виконання цього прикладу:

```
Версия CUBRID PHP:             9.1.0.0001

PARAM_ISOLATION_LEVEL          3
LOCK_TIMEOUT                   -1
MAX_STRING_LENGTH              1073741823
PARAM_AUTO_COMMIT              1

Информация о сервере:          9.1.0.0212
Информация о клиенте:          9.1.0

Кодировка CUBRID:              iso8859-1
```