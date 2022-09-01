---
navigation:
  - function.cubrid-connect-with-url.html: « cubridconnectwithurl
  - function.cubrid-current-oid.html: cubridcurrentoid »
  - index.md: PHP Manual
  - ref.cubrid.md: Функции CUBRID
title: cubridconnect
---
# cubridconnect

(PECL CUBRID >= 8.3.1)

cubridconnect — Відкриває з'єднання з сервером CUBRID

### Опис

```methodsynopsis
cubrid_connect(    string $host,    int $port,    string $dbname,    string $userid = ?,    string $passwd = ?,    bool $new_link = false): resource
```

Функція **cubridconnect()** використовується для створення з'єднання з сервером, використовуючи його адресу, порт, ім'я бази даних, ім'я користувача та пароля. Якщо логін та пароль не задані, то за умовчанням використовуватиметься з'єднання "PUBLIC".

### Список параметрів

`host`

Ім'я хоста або IP-адреса сервера CUBRID CAS.

`port`

Порт сервера CUBRID CAS (BROKERPORT у $CUBRID/conf/cubridbroker.conf).

`dbname`

Назва бази даних.

`userid`

Ім'я користувача. Якщо не встановлено, то буде використано ім'я за промовчанням "public".

`passwd`

Пароль. Якщо не заданий, то використовуватиметься "".

`new_link`

Якщо функція [cubridconnectwithurl()](function.cubrid-connect-with-url.html) була викликана повторно з такими ж аргументами, нове з'єднання не буде створено, замість нього буде повернено ідентифікатор вже підключення. Параметр `new_link` змінює таку поведінку і змушує [cubridconnectwithurl()](function.cubrid-connect-with-url.html) у будь-якому випадку створити нове з'єднання, навіть якщо функція [cubridconnectwithurl()](function.cubrid-connect-with-url.html) раніше була викликана з такими самими аргументами.

### Значення, що повертаються

Ідентифікатор підключення у разі успішного виконання або **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання **cubridconnect()****

```php
<?php
printf("%-30s %s\n", "CUBRID PHP Version:", cubrid_version());

printf("\n");

$conn = cubrid_connect("localhost", 33000, "demodb", "dba");

if (!$conn) {
    die('Connect Error ('. cubrid_error_code() .')' . cubrid_error_msg());
}

$db_params = cubrid_get_db_parameter($conn);

while (list($param_name, $param_value) = each($db_params)) {
    printf("%-30s %s\n", $param_name, $param_value);
}

printf("\n");

$server_info = cubrid_get_server_info($conn);
$client_info = cubrid_get_client_info();

printf("%-30s %s\n", "Server Info:", $server_info);
printf("%-30s %s\n", "Client Info:", $client_info);

printf("\n");

$charset = cubrid_get_charset($conn);

printf("%-30s %s\n", "CUBRID Charset:", $charset);

cubrid_disconnect($conn);
?>
```

Результат виконання цього прикладу:

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

-   [cubridpconnect()](function.cubrid-pconnect.html) - Відкриває постійне з'єднання із сервером CUBRID
-   [cubridconnectwithurl()](function.cubrid-connect-with-url.html) - Створює оточення для з'єднання із сервером CUBRID
-   [cubridpconnectwithurl()](function.cubrid-pconnect-with-url.html) - Відкриває постійне з'єднання із сервером CUBRID
-   [cubriddisconnect()](function.cubrid-disconnect.html) - Закриває з'єднання з базою даних
-   [cubridclose()](function.cubrid-close.html) - Закриває з'єднання з базою даних
