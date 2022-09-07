---
navigation:
  - function.mysql-close.md: « mysqlclose
  - function.mysql-create-db.md: mysqlcreatedb »
  - index.md: PHP Manual
  - ref.mysql.md: MySQL
title: mysqlconnect
---
# mysqlconnect

(PHP 4, PHP 5)

mysqlconnect — Відкриває з'єднання з сервером MySQL

**Увага**

Цей модуль застарів, починаючи з версії PHP 5.5.0, і вилучений у PHP 7.0.0. Використовуйте замість нього [MySQLi](book.mysqli.md) або [PDOMySQL](ref.pdo-mysql.md). Дивіться також інструкцію [MySQL: вибір API](mysqlinfo.api.choosing.md). Альтернативи для цієї функції:

-   [mysqliconnect()](function.mysqli-connect.md)
-   [PDO::construct()](pdo.construct.md)

### Опис

```methodsynopsis
mysql_connect(    string $server = ini_get("mysql.default_host"),    string $username = ini_get("mysql.default_user"),    string $password = ini_get("mysql.default_password"),    bool $new_link = false,    int $client_flags = 0): resource|false
```

Відкриває нове з'єднання з MySQL сервером або використовує вже існуюче.

### Список параметрів

`server`

Сервер MySQL. Може також включати номер порту, наприклад "hostname:port" або шлях до локального сокету, наприклад ":/path/to/socket" для локального сервера.

Якщо PHP-директива [mysql.defaulthost](mysql.configuration.md#ini.mysql.default-host) не визначена (за умовчанням), то значенням за промовчанням є 'localhost:3306'. У [SQL safe mode](ini.core.md#ini.sql.safe-mode) цей параметр ігнорується і завжди використовується значення 'localhost:3306'.

`username`

Ім'я користувача. Значення за умовчанням визначається директивою [mysql.defaultuser](mysql.configuration.md#ini.mysql.default-user). У [SQL safe mode](ini.core.md#ini.sql.safe-mode) цей параметр буде проігнорований і буде використаний користувач, який володіє процесом сервера.

`password`

Пароль. Значення за умовчанням визначається директивою [mysql.defaultpassword](mysql.configuration.md#ini.mysql.default-password). У [SQL safe mode](ini.core.md#ini.sql.safe-mode) цей параметр буде проігноровано і як пароль буде використано порожній рядок.

`new_link`

Якщо другий виклик функції **mysqlconnect()** стався з тими самими аргументами, то нове з'єднання не буде встановлено. Натомість функція поверне посилання на вже встановлене з'єднання. Параметр `new_link` може змусити функцію **mysqlconnect()** відкрити ще одне з'єднання, навіть якщо з'єднання з аналогічними параметрами вже відкрито. У [SQL safe mode](ini.core.md#ini.sql.safe-mode) цей параметр ігнорується.

`client_flags`

Параметр `client_flags` має бути комбінацією з наступних констант: 128 (включає обробку `LOAD DATA LOCAL` **`MYSQL_CLIENT_SSL`** **`MYSQL_CLIENT_COMPRESS`** **`MYSQL_CLIENT_IGNORE_SPACE`** ор **`MYSQL_CLIENT_INTERACTIVE`**. Детальніше читайте у розділі [Клієнтські константи MySQL](mysql.constants.md#mysql.client-flags). У [SQL safe mode](ini.core.md#ini.sql.safe-mode) цей параметр ігнорується.

### Значення, що повертаються

Повертає дескриптор з'єднання з MySQL у разі успішного виконання або **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання **mysqlconnect()****

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

**Приклад #2 Приклад використання **mysqlconnect()** із синтаксисом `hostname:port`**

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

**Приклад #3 Приклад використання **mysqlconnect()** із синтаксисом ":/path/to/socket"**

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

> **Зауваження**
> 
> Якщо вказати параметр `server` значення "localhost" або "localhost:port" клієнтська бібліотека MySQL намагатиметься з'єднатися з локальним сокетом. Якщо ви все ж таки хочете використовувати TCP/IP, використовуйте адресу "127.0.0.1" замість "localhost". Якщо клієнтська бібліотека намагається підключитися не до локального сокету, правильний шлях повинен бути встановлений через вказівку директиви php.ini [mysql.defaulthost](mysql.configuration.md#ini.mysql.default-host) у php.ini, після чого можна залишати параметр `server` порожній.

> **Зауваження**
> 
> З'єднання з сервером буде закрито після завершення виконання скрипту, якщо тільки до цього воно не було закрито за допомогою функції [mysqlclose()](function.mysql-close.md)

> **Зауваження**
> 
> Помилка "Can't create TCP/IP socket (10106)" (Неможливо створити сокет TCP/IP) зазвичай означає, що конфігураційна директива [variablesorder](ini.core.md#ini.variables-order) не містить символ `E`. У Windows, якщо в оточенні не буде скопійовано змінне оточення `SYSTEMROOT`, то PHP буде мати проблеми при завантаженні Winsock.

### Дивіться також

-   [mysqlpconnect()](function.mysql-pconnect.md) - Встановлює постійне з'єднання із сервером MySQL
-   [mysqlclose()](function.mysql-close.md) - Закриває з'єднання із сервером MySQL
