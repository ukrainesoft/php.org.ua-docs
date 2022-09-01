---
navigation:
  - function.cubrid-pconnect-with-url.html: « cubridpconnectwithurl
  - function.cubrid-prepare.html: cubridprepare »
  - index.md: PHP Manual
  - ref.cubrid.md: Функции CUBRID
title: cubridpconnect
---
# cubridpconnect

(PECL CUBRID >= 8.3.1)

cubridpconnect — Відкриває постійне з'єднання із сервером CUBRID

### Опис

```methodsynopsis
cubrid_pconnect(    string $host,    int $port,    string $dbname,    string $userid = ?,    string $passwd = ?): resource
```

Встановлює постійне з'єднання із сервером CUBRID.

**cubridpconnect()** діє дуже схоже на [cubridconnect()](function.cubrid-connect.html) з двома основними відмінностями:

По-перше, при підключенні функція спочатку спробує знайти (постійне) посилання, яке вже відкрито з тим самим хостом, портом, ім'ям бази даних та ідентифікатором користувача. Якщо з'єднання знайдено, замість відкриття нового буде повернуто його ідентифікатор.

По-друге, з'єднання з SQL-сервером не буде закрито після закінчення скрипту. Натомість посилання залишиться відкритим для використання в майбутньому ([cubridclose()](function.cubrid-close.html) або [cubriddisconnect()](function.cubrid-disconnect.html) не закриє посилання, встановлені **cubridpconnect()**

Тому цей тип посилання називається "постійним".

### Список параметрів

`host`

Ім'я хоста або IP-адреса сервера CUBRID CAS.

`port`

Номер порту CUBRID CAS-сервера (BROKERPORT налаштований у $CUBRID/conf/cubridbroker.conf).

`dbname`

Назва бази даних.

`userid`

Ім'я користувача бази даних.

`passwd`

Пароль користувача.

### Значення, що повертаються

Ідентифікатор з'єднання у разі успішного виконання процесу або **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання [cubridconnect()](function.cubrid-connect.html)**

```php
<?php
printf("%-30s %s\n", "Версия PHP CUBRID:", cubrid_version());

printf("\n");

$conn = cubrid_pconnect("localhost", 33000, "demodb", "dba");

if (!$conn) {
    die('Ошибка соединения ('. cubrid_error_code() .')' . cubrid_error_msg());
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
Версия PHP CUBRID:             9.1.0.0001

PARAM_ISOLATION_LEVEL          3
LOCK_TIMEOUT                   -1
MAX_STRING_LENGTH              1073741823
PARAM_AUTO_COMMIT              1

Информация о сервере:             9.1.0.0212
Информация о клиенте:             9.1.0

Кодировка CUBRID:                iso8859-1
```

### Дивіться також

-   [cubridconnect()](function.cubrid-connect.html) - Відкриває з'єднання з сервером CUBRID
-   [cubridconnectwithurl()](function.cubrid-connect-with-url.html) - Створює оточення для з'єднання із сервером CUBRID
-   [cubridpconnectwithurl()](function.cubrid-pconnect-with-url.html) - Відкриває постійне з'єднання із сервером CUBRID
-   [cubriddisconnect()](function.cubrid-disconnect.html) - Закриває з'єднання з базою даних
-   [cubridclose()](function.cubrid-close.html) - Закриває з'єднання з базою даних
