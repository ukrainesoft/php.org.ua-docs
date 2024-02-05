---
navigation:
  - function.cubrid-pconnect-with-url.md: « cubrid\_pconnect\_with\_url
  - function.cubrid-prepare.md: cubrid\_prepare »
  - index.md: PHP Manual
  - ref.cubrid.md: Функції CUBRID
title: cubrid\_pconnect
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# cubrid\_pconnect

(PECL CUBRID >= 8.3.1)

cubrid\_pconnect — Відкриває постійне з'єднання із сервером CUBRID

### Опис

```methodsynopsis
cubrid_pconnect(    string $host,    int $port,    string $dbname,    string $userid = ?,    string $passwd = ?): resource
```

Встановлює постійне з'єднання із сервером CUBRID.

**cubrid\_pconnect()** діє дуже схоже на [cubrid\_connect()](function.cubrid-connect.md) з двома основними відмінностями:

По-перше, при підключенні функція спочатку спробує знайти (постійне) посилання, яке вже відкрито з тим самим хостом, портом, ім'ям бази даних та ідентифікатором користувача. Якщо з'єднання буде знайдено, замість відкриття нового буде повернуто його ідентифікатор.

По-друге, з'єднання з SQL-сервером не буде закрито після закінчення скрипту. Натомість посилання залишиться відкритим для використання в майбутньому ([cubrid\_close()](function.cubrid-close.md) або [cubrid\_disconnect()](function.cubrid-disconnect.md) не закриє посилання, встановлені **cubrid\_pconnect()**

Тому цей тип посилання називається "постійним".

### Список параметрів

`host`

Ім'я хоста або IP-адреса сервера CUBRID CAS.

`port`

Номер порту CUBRID CAS-сервера (BROKER\_PORT налаштований у $CUBRID/conf/cubrid\_broker.conf).

`dbname`

Назва бази даних.

`userid`

Ім'я користувача бази даних.

`passwd`

Пароль користувача.

### Значення, що повертаються

Ідентифікатор з'єднання у разі успішного виконання процесу або \*\*`false`\*\*в случае возникновения ошибки.

### Приклади

**Приклад #1 Приклад использования[cubrid\_connect()](function.cubrid-connect.md)**

```php
<?php
printf("%-30s %s\n", "Версия PHP CUBRID:", cubrid_version());

printf("\n");

$conn = cubrid_pconnect("localhost", 33000, "demodb", "dba");

if (!$conn) {
    die('Ошибка соединения ('. cubrid_error_code() .')' . cubrid_error_msg());
}

$db_params = cubrid_get_db_parameter($conn);

while (list($param_name, $param_value) = each($db_params)) {
    printf("%-30s %s\n", $param_name, $param_value);
}

printf("\n");

$server_info = cubrid_get_server_info($conn);
$client_info = cubrid_get_client_info();

printf("%-30s %s\n", "Информация о сервере:", $server_info);
printf("%-30s %s\n", "Информация о клиенте:", $client_info);

printf("\n");

$charset = cubrid_get_charset($conn);

printf("%-30s %s\n", "Кодировка CUBRID:", $charset);

cubrid_disconnect($conn);
?>
```

Результат виконання наведеного прикладу:

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

-   [cubrid\_connect()](function.cubrid-connect.md) \- Відкриває з'єднання з сервером CUBRID
-   [cubrid\_connect\_with\_url()](function.cubrid-connect-with-url.md) \- Створює оточення для з'єднання із сервером CUBRID
-   [cubrid\_pconnect\_with\_url()](function.cubrid-pconnect-with-url.md) \- Відкриває постійне з'єднання із сервером CUBRID
-   [cubrid\_disconnect()](function.cubrid-disconnect.md) \- Закриває з'єднання з базою даних
-   [cubrid\_close()](function.cubrid-close.md) \- Закриває з'єднання з базою даних
