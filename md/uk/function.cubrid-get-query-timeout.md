---
navigation:
  - function.cubrid-get-db-parameter.md: « cubrid\_get\_db\_parameter
  - function.cubrid-get-server-info.md: cubrid\_get\_server\_info »
  - index.md: PHP Manual
  - ref.cubrid.md: Функції CUBRID
title: cubrid\_get\_query\_timeout
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# cubrid\_get\_query\_timeout

(PECL CUBRID >= 8.4.1)

cubrid\_get\_query\_timeout — Отримує значення часу очікування запиту

### Опис

```methodsynopsis
cubrid_get_query_timeout(resource $req_identifier): int
```

Функция\*\*cubrid\_get\_query\_timeout()\*\*используется для получения времени ожидания запроса.

### Список параметрів

`req_identifier`

Ідентифікатор запиту.

### Значення, що повертаються

Повертає значення часу очікування поточного запиту у мілісекундах у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Приклади

**Приклад #1 Приклад використання** cubrid\_get\_query\_timeout()\*\*\*\*

```php
<?php

$host = "localhost";
$port = 33000;
$db = "demodb";

$conn =
cubrid_connect_with_url("CUBRID:$host:$port:$db:::?login_timeout=50000&query_timeout=5000&disconnect_on_query_timeout=yes");

$req = cubrid_prepare($conn, "SELECT * FROM code");

$timeout = cubrid_get_query_timeout($req);
var_dump($timeout);

cubrid_set_query_timeout($req, 1000);
$timeout = cubrid_get_query_timeout($req);
var_dump($timeout);

cubrid_close($conn);
?>
```

Результат виконання наведеного прикладу:

```
int(5000)
int(1000)
```

### Дивіться також

-   [cubrid\_set\_query\_timeout()](function.cubrid-set-query-timeout.md) \- Встановлює час очікування на виконання запиту
