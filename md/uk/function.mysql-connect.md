---
navigation:
  - function.mysql-close.md: « mysql\_close
  - function.mysql-create-db.md: mysql\_create\_db »
  - index.md: PHP Manual
  - ref.mysql.md: MySQL
title: mysql\_connect
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# mysql\_connect

(PHP 4, PHP 5)

mysql\_connect — Відкриває з'єднання з сервером MySQL

**Увага**

Цей модуль застарів, починаючи з версії PHP 5.5.0, і видалений у PHP 7.0.0. Використовуйте замість нього [MySQLi](book.mysqli.md) або [PDO\_MySQL](ref.pdo-mysql.md)Смотрите также инструкцию[MySQL: вибір API](mysqlinfo.api.choosing.md). Альтернативи для цієї функції:

-   [mysqli\_connect()](function.mysqli-connect.md)
-   [PDO::\_\_construct()](pdo.construct.md)

### Опис

```methodsynopsis
mysql_connect(    string $server = ini_get("mysql.default_host"),    string $username = ini_get("mysql.default_user"),    string $password = ini_get("mysql.default_password"),    bool $new_link = false,    int $client_flags = 0): resource|false
```

Відкриває нове з'єднання з сервером MySQL або використовує існуюче.

### Список параметрів

`server`

Сервер MySQL. Може також включати номер порту, наприклад "hostname:port" або шлях до локального сокету, наприклад ":/path/to/socket" для локального сервера.

Якщо PHP-директива [mysql.default\_host](mysql.configuration.md#ini.mysql.default-host) не визначена (за умовчанням), то значенням за промовчанням є 'localhost:3306'. У [SQL safe mode](ini.core.md#ini.sql.safe-mode) цей параметр ігнорується і завжди використовується значення 'localhost:3306'.

`username`

Ім'я користувача. Значення за умовчанням визначається директивою [mysql.default\_user](mysql.configuration.md#ini.mysql.default-user). [SQL safe mode](ini.core.md#ini.sql.safe-mode) цей параметр буде проігнорований і буде використаний користувач, який володіє процесом сервера.

`password`

Пароль. Значення за умовчанням визначається директивою [mysql.default\_password](mysql.configuration.md#ini.mysql.default-password). [SQL safe mode](ini.core.md#ini.sql.safe-mode) цей параметр буде проігноровано і як пароль буде використано порожній рядок.

`new_link`

Якщо другий виклик функції **mysql\_connect()** стався з тими самими аргументами, то нове з'єднання не буде встановлено. Натомість функція поверне посилання на вже встановлене з'єднання. Параметр `new_link` може змусити функцію **mysql\_connect()** відкрити ще одне з'єднання, навіть якщо з'єднання з аналогічними параметрами вже відкрито. У [SQL safe mode](ini.core.md#ini.sql.safe-mode) цей параметр ігнорується.

`client_flags`

Параметр`client_flags` має бути комбінацією з наступних констант: 128 (включає обробку `LOAD DATA LOCAL` **`MYSQL_CLIENT_SSL`** **`MYSQL_CLIENT_COMPRESS`** **`MYSQL_CLIENT_IGNORE_SPACE`**or**`MYSQL_CLIENT_INTERACTIVE`**. Детальніше читайте у розділі [Клієнтські константи MySQL](mysql.constants.md#mysql.client-flags). [SQL safe mode](ini.core.md#ini.sql.safe-mode) цей параметр ігнорується.

### Значення, що повертаються

Повертає дескриптор з'єднання з MySQL у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Приклади

**Приклад #1 Приклад використання** mysql\_connect()\*\*\*\*

```php
<?php
$link = mysql_connect('localhost', 'mysql_user', 'mysql_password');
if (!$link) {
    die('Ошибка соединения: ' . mysql_error());
}
echo 'Успешно соединились';
mysql_close($link);
?>
```

**Приклад #2 Приклад використання** mysql\_connect()\*\* із синтаксисом `hostname:port`\*\*

```php
<?php
// соединяемся с example.com на порту 3307
$link = mysql_connect('example.com:3307', 'mysql_user', 'mysql_password');
if (!$link) {
    die('Ошибка соединения: ' . mysql_error());
}
echo 'Успешно соединились';
mysql_close($link);

// соединяемся с localhost на порту 3307
$link = mysql_connect('127.0.0.1:3307', 'mysql_user', 'mysql_password');
if (!$link) {
    die('Ошибка соединения: ' . mysql_error());
}
echo 'Успешно соединились';
mysql_close($link);
?>
```

**Приклад #3 Приклад використання** mysql\_connect()\*\* із синтаксисом ":/path/to/socket"\*\*

```php
<?php
// соединяемся к localhost по сокету, т.е. /tmp/mysql.sock

// вариант 1: не указываем localhost
$link = mysql_connect(':/tmp/mysql', 'mysql_user', 'mysql_password');
if (!$link) {
    die('Ошибка соединения: ' . mysql_error());
}
echo 'Успешно соединились';
mysql_close($link);


// вариант 2: указываем localhost
$link = mysql_connect('localhost:/tmp/mysql.sock', 'mysql_user', 'mysql_password');
if (!$link) {
    die('Ошибка соединения: ' . mysql_error());
}
echo 'Успешно соединились';
mysql_close($link);
?>
```

### Примітки

> **Зауваження** :
> 
> При указании параметру`server` значення "localhost" або "localhost:port" клієнтська бібліотека MySQL намагатиметься з'єднатися з локальним сокетом. Якщо ви все ж таки хочете використовувати TCP/IP, використовуйте адресу "127.0.0.1" замість "localhost". Якщо клієнтська бібліотека намагається підключитися не до локального сокету, правильний шлях повинен бути встановлений через вказівку директиви php.ini [mysql.default\_host](mysql.configuration.md#ini.mysql.default-host)в php.ini, после чего можно оставлять параметр`server` порожній.

> **Зауваження** :
> 
> З'єднання з сервером буде закрито після завершення виконання скрипту, якщо тільки до цього воно не було закрито за допомогою функції [mysql\_close()](function.mysql-close.md)

> **Зауваження** :
> 
> Помилка "Can't create TCP/IP socket (10106)" (Неможливо створити сокет TCP/IP) зазвичай означає, що конфігураційна директива [variables\_order](ini.core.md#ini.variables-order) не містить символ `E`. У Windows, якщо в оточенні не буде скопійовано змінне оточення `SYSTEMROOT`, то PHP буде мати проблеми при завантаженні Winsock.

### Дивіться також

-   [mysql\_pconnect()](function.mysql-pconnect.md) \- Встановлює постійне з'єднання із сервером MySQL
-   [mysql\_close()](function.mysql-close.md) \- Закриває з'єднання із сервером MySQL
