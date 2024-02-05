---
navigation:
  - function.mysql-num-rows.md: « mysql\_num\_rows
  - function.mysql-ping.md: mysql\_ping »
  - index.md: PHP Manual
  - ref.mysql.md: MySQL
title: mysql\_pconnect
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# mysql\_pconnect

(PHP 4, PHP 5)

mysql\_pconnect — Встановлює постійне з'єднання з сервером MySQL

**Увага**

Цей модуль застарів, починаючи з версії PHP 5.5.0, і видалений у PHP 7.0.0. Використовуйте замість нього [MySQLi](book.mysqli.md) або [PDO\_MySQL](ref.pdo-mysql.md)Смотрите также инструкцию[MySQL: вибір API](mysqlinfo.api.choosing.md). Альтернативи для цієї функції:

-   [mysqli\_connect()](function.mysqli-connect.md)с`p:`префіксом хоста
-   [PDO::\_\_construct()](pdo.construct.md)з опцією драйвера\*\*`PDO::ATTR_PERSISTENT`\*\*

### Опис

```methodsynopsis
mysql_pconnect(    string $server = ini_get("mysql.default_host"),    string $username = ini_get("mysql.default_user"),    string $password = ini_get("mysql.default_password"),    int $client_flags = 0): resource
```

Встановлює постійне з'єднання із сервером MySQL.

**mysql\_pconnect()** працює аналогічно [mysql\_connect()](function.mysql-connect.md) із двома важливими відмінностями.

По-перше, при з'єднанні функція намагається знайти вже відкритий (постійний) покажчик на той самий сервер із тим самим користувачем та паролем. Якщо він знайдений, повернутий функцією буде саме він замість відкриття нового з'єднання.

По-друге, з'єднання з SQL-сервером не буде закрито, коли робота скрипта закінчиться. Натомість, воно залишиться робочим для майбутнього використання ([mysql\_close()](function.mysql-close.md) також не закриває постійні з'єднання, відкриті **mysql\_pconnect()**

З'єднання такого типу називають "постійними".

### Список параметрів

`server`

Сервер MySQL. Може також включати номер порту, наприклад "hostname:port" або шлях до локального сокету, наприклад ":/path/to/socket" для локального хоста.

Якщо директива [mysql.default\_host](mysql.configuration.md#ini.mysql.default-host) не визначено (за умовчанням), то за замовчуванням використовується значення 'localhost:3306'

`username`

Ім'я користувача. За промовчанням використовується ім'я користувача, який володіє серверним процесом.

`password`

Пароль. За промовчанням використовується порожній рядок.

`client_flags`

Параметр`client_flags` може бути комбінацією наступних констант: 128 (включає обробку `LOAD DATA LOCAL` **`MYSQL_CLIENT_SSL`** **`MYSQL_CLIENT_COMPRESS`** **`MYSQL_CLIENT_IGNORE_SPACE`** і **`MYSQL_CLIENT_INTERACTIVE`**

### Значення, що повертаються

Повертає дескриптор постійного з'єднання MySQL у разі успішного виконання, та \*\*`false`\*\*в случае возникновения ошибки.

### Примітки

> **Зауваження** :
> 
> Зверніть увагу, що з'єднання такого типу працюють тільки, якщо PHP встановлений як модуль. За додатковою інформацією звертайтесь до розділу " [Постійні з'єднання з базами даних](features.persistent-connections.md) ".

**Увага**

Використання постійних з'єднань може вимагати деякої настройки Apache та MySQL. Переконайтеся, що ви не перевищите максимальну кількість дозволених з'єднань MySQL.

### Дивіться також

-   [mysql\_connect()](function.mysql-connect.md) \- Відкриває з'єднання із сервером MySQL
-   " [Постійні з'єднання з базами даних](features.persistent-connections.md) "
