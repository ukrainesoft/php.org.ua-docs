---
navigation:
  - function.mysql-num-rows.html: « mysqlnumrows
  - function.mysql-ping.html: mysqlping »
  - index.md: PHP Manual
  - ref.mysql.md: MySQL
title: mysqlpconnect
---
# mysqlpconnect

(PHP 4, PHP 5)

mysqlpconnect — Встановлює постійне з'єднання з сервером MySQL

**Увага**

Цей модуль застарів, починаючи з версії PHP 5.5.0, і вилучений у PHP 7.0.0. Використовуйте замість нього [MySQLi](book.mysqli.md) або [PDOMySQL](ref.pdo-mysql.md). Дивіться також інструкцію [MySQL: вибір API](mysqlinfo.api.choosing.md). Альтернативи для цієї функції:

-   [mysqliconnect()](function.mysqli-connect.md) з `p:` префіксом хоста
-   [PDO::construct()](pdo.construct.md) з опцією драйвера **`PDO::ATTR_PERSISTENT`**

### Опис

```methodsynopsis
mysql_pconnect(    string $server = ini_get("mysql.default_host"),    string $username = ini_get("mysql.default_user"),    string $password = ini_get("mysql.default_password"),    int $client_flags = 0): resource
```

Встановлює постійне з'єднання із сервером MySQL.

**mysqlpconnect()** працює аналогічно [mysqlconnect()](function.mysql-connect.md) із двома важливими відмінностями.

По-перше, при з'єднанні функція намагається знайти вже відкритий (постійний) покажчик на той самий сервер із тим самим користувачем та паролем. Якщо він знайдений, повернутий функцією буде саме він замість відкриття нового з'єднання.

По-друге, з'єднання з SQL-сервером не буде закрито, коли робота скрипта закінчиться. Натомість, воно залишиться робочим для майбутнього використання ([mysqlclose()](function.mysql-close.md) також не закриває постійні з'єднання, відкриті **mysqlpconnect()**

З'єднання такого типу називають "постійними".

### Список параметрів

`server`

Сервер MySQL. Може також включати номер порту, наприклад "hostname:port" або шлях до локального сокету, наприклад ":/path/to/socket" для локального хоста.

Якщо директива [mysql.defaulthost](mysql.configuration.html#ini.mysql.default-host) не визначено (за умовчанням), то за замовчуванням використовується значення 'localhost:3306'

`username`

Ім'я користувача. За промовчанням використовується ім'я користувача, який володіє серверним процесом.

`password`

Пароль. За промовчанням використовується порожній рядок.

`client_flags`

Параметр `client_flags` може бути комбінацією наступних констант: 128 (включає обробку `LOAD DATA LOCAL` **`MYSQL_CLIENT_SSL`** **`MYSQL_CLIENT_COMPRESS`** **`MYSQL_CLIENT_IGNORE_SPACE`** і **`MYSQL_CLIENT_INTERACTIVE`**

### Значення, що повертаються

Повертає дескриптор постійного з'єднання MySQL у разі успішного виконання, та **`false`** у разі виникнення помилки.

### Примітки

> **Зауваження**
> 
> Зверніть увагу, що з'єднання такого типу працюють тільки, якщо PHP встановлений як модуль. За додатковою інформацією звертайтесь до розділу "[Постійні з'єднання з базами даних](features.persistent-connections.md)".

**Увага**

Використання постійних з'єднань може вимагати деякої настройки Apache та MySQL. Переконайтеся, що ви не перевищите максимальну кількість дозволених з'єднань MySQL.

### Дивіться також

-   [mysqlconnect()](function.mysql-connect.md) - Відкриває з'єднання із сервером MySQL
-   "[Постійні з'єднання з базами даних](features.persistent-connections.md)"
