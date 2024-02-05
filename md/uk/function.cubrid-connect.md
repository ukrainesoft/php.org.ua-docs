---
navigation:
  - function.cubrid-connect-with-url.md: « cubrid\_connect\_with\_url
  - function.cubrid-current-oid.md: cubrid\_current\_oid »
  - index.md: PHP Manual
  - ref.cubrid.md: Функції CUBRID
title: cubrid\_connect
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# cubrid\_connect

(PECL CUBRID >= 8.3.1)

cubrid\_connect — Відкриває з'єднання з сервером CUBRID

### Опис

```methodsynopsis
cubrid_connect(    string $host,    int $port,    string $dbname,    string $userid = ?,    string $passwd = ?,    bool $new_link = false): resource
```

Функция**cubrid\_connect()** використовується для створення з'єднання з сервером, використовуючи його адресу, порт, ім'я бази даних, ім'я користувача та пароля. Якщо логін та пароль не задані, то за умовчанням використовуватиметься з'єднання "PUBLIC".

### Список параметрів

`host`

Ім'я хоста або IP-адреса сервера CUBRID CAS.

`port`

Порт сервера CUBRID CAS (BROKER\_PORT у $CUBRID/conf/cubrid\_broker.conf).

`dbname`

Назва бази даних.

`userid`

Ім'я користувача. Якщо не встановлено, то буде використано ім'я за промовчанням "public".

`passwd`

Пароль. Якщо не заданий, то використовуватиметься "".

`new_link`

Якщо функція [cubrid\_connect\_with\_url()](function.cubrid-connect-with-url.md) була викликана повторно з такими ж аргументами, нове з'єднання не буде створено, замість нього буде повернено ідентифікатор вже підключення. Параметр `new_link` змінює таку поведінку і змушує [cubrid\_connect\_with\_url()](function.cubrid-connect-with-url.md) у будь-якому випадку створити нове з'єднання, навіть якщо функція [cubrid\_connect\_with\_url()](function.cubrid-connect-with-url.md) раніше була викликана з такими самими аргументами.

### Значення, що повертаються

Ідентифікатор підключення у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Приклади

**Приклад #1 Приклад використання** cubrid\_connect()\*\*\*\*

```php
<?php
printf("%-30s %s\n", "CUBRID PHP Version:", cubrid_version());

printf("\n");

$conn = cubrid_connect("localhost", 33000, "demodb", "dba");

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

-   [cubrid\_pconnect()](function.cubrid-pconnect.md) \- Відкриває постійне з'єднання із сервером CUBRID
-   [cubrid\_connect\_with\_url()](function.cubrid-connect-with-url.md) \- Створює оточення для з'єднання із сервером CUBRID
-   [cubrid\_pconnect\_with\_url()](function.cubrid-pconnect-with-url.md) \- Відкриває постійне з'єднання із сервером CUBRID
-   [cubrid\_disconnect()](function.cubrid-disconnect.md) \- Закриває з'єднання з базою даних
-   [cubrid\_close()](function.cubrid-close.md) \- Закриває з'єднання з базою даних
