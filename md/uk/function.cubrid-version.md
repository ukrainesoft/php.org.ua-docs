---
navigation:
  - function.cubrid-set-query-timeout.md: « cubrid\_set\_query\_timeout
  - cubridmysql.cubrid.md: Функції сумісності CUBRID MySQL »
  - index.md: PHP Manual
  - ref.cubrid.md: Функції CUBRID
title: cubrid\_version
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# cubrid\_version

(PECL CUBRID >= 8.3.0)

cubrid\_version — Отримати версію модуля CUBRID PHP

### Опис

```methodsynopsis
cubrid_version(): string
```

Функция**cubrid\_version()** використовується для отримання версії CUBRID PHP.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Інформація про версію (наприклад, "8.3.1.0001").

### Приклади

**Приклад #1 Приклад використання** cubrid\_version()\*\*\*\*

```php
<?php
printf("%-30s %s\n", "CUBRID PHP Version:", cubrid_version());

printf("\n");

$conn = cubrid_connect("localhost", 33088, "demodb", "dba");

if (!$conn) {
    die('Connect Error ('. cubrid_error_code() .')' . cubrid_error_msg());
}

$db_params = cubrid_get_db_parameter($conn);

while (list($param_name, $param_value) = each($db_params)) {
    printf("%-30s %s\n", $param_name, $param_value);
}

printf("\n");

$server_info = cubrid_get_server_info($conn);
$client_info = cubrid_get_client_info();

printf("%-30s %s\n", "Server Info:", $server_info);
printf("%-30s %s\n", "Client Info:", $client_info);

printf("\n");

$charset = cubrid_get_charset($conn);

printf("%-30s %s\n", "CUBRID Charset:", $charset);

cubrid_disconnect($conn);

?>
```

Результат виконання наведеного прикладу:

```
CUBRID PHP Version:            9.1.0.0001

PARAM_ISOLATION_LEVEL          3
LOCK_TIMEOUT                   -1
MAX_STRING_LENGTH              1073741823
PARAM_AUTO_COMMIT              1

Server Info:                   9.1.0.0212
Client Info:                   9.1.0

CUBRID Charset:                iso8859-1
```

### Дивіться також

-   [cubrid\_error\_code()](function.cubrid-error-code.md) \- Отримати код помилки
-   [cubrid\_error\_code\_facility()](function.cubrid-error-code-facility.md) \- Отримати код рівня, на якому сталася помилка
