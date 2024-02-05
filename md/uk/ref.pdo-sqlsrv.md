---
navigation:
  - ref.pdo-mysql.connection.md: « PDO\_MYSQL DSN
  - ref.pdo-sqlsrv.connection.md: PDO\_SQLSRV DSN »
  - index.md: PHP Manual
  - pdo.drivers.md: Драйвери PDO
title: Функції модуля PDO\_SQLSRV для Microsoft SQL Server
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Функції модуля PDO\_SQLSRV для Microsoft SQL Server

## Вступ

PDO\_SQLSRV - це драйвер, що реалізує інтерфейс [PHP Data Objects (PDO)](intro.pdo.md) для отримання доступу з PHP до баз даних MS SQL Server (починаючи з версії SQL Server 2005) та SQL Azure.

## Установка

Остання версія драйвера доступна для завантаження за посиланням: [» Завантаження SQLSRV](http://msdn.microsoft.com/en-us/sqlserver/ff657782.aspx). Вихідний код драйвера розміщено в [» публічній репозиторії](https://github.com/microsoft/msphpsql)

За детальною інформацією про системні вимоги зверніться до розділу [» Системні вимоги SQLSRV](http://msdn.microsoft.com/en-us/library/cc296170.aspx)

У Windows модуль PDO\_SQLSRV включається шляхом завантаження та додавання необхідних DLL-файлів у каталог модулів PHP та додавання до файлу php.ini запису, який завантажить модуль.

У Linux та macOS модуль PDO\_SQLSRV можно установить из библиотеки[» PECL](https://pecl.php.net/)Подробности смотрите в[» посібнику з встановлення](https://docs.microsoft.com/en-us/sql/connect/php/installation-tutorial-linux-mac)

## Обумовлені константи

Наведені нижче константи визначені цим драйвером і будуть доступні лише у випадку, якщо PHP був зібраний за допомогою цього модуля, або модуль був динамічно завантажений під час виконання. Крім того, ці залежні від драйвера константи повинні бути використані лише разом із цим драйвером. Використання атрибутів, специфічних для деякого драйвера з іншим драйвером, може викликати несподівану поведінку. Якщо ваш код виконується з кількома драйверами, можна використовувати функцію [PDO::getAttribute()](pdo.getattribute.md)для получения атрибута\*\*`PDO::ATTR_DRIVER_NAME`\*\*для проверки драйвера.

**`PDO::SQLSRV_TXN_READ_UNCOMMITTED`**(int)

Ця константа - допустиме значення для ключа TransactionIsolation SQLSRV DSN. Встановлює рівень ізоляції транзакцій для з'єднання значення Read Uncommitted.

**`PDO::SQLSRV_TXN_READ_COMMITTED`**(int)

Ця константа - допустиме значення для ключа TransactionIsolation SQLSRV DSN. Встановлює рівень ізоляції транзакцій для з'єднання значення Read Committed.

**`PDO::SQLSRV_TXN_REPEATABLE_READ`**(int)

Ця константа - допустиме значення для ключа TransactionIsolation SQLSRV DSN. Встановлює рівень ізоляції транзакцій для з'єднання значення Repeateable Read.

**`PDO::SQLSRV_TXN_SNAPSHOT`**(int)

Ця константа - допустиме значення для ключа TransactionIsolation SQLSRV DSN. Встановлює рівень ізоляції транзакцій для з'єднання значення Snapshot.

**`PDO::SQLSRV_TXN_SERIALIZABLE`**(int)

Ця константа - допустиме значення для ключа TransactionIsolation SQLSRV DSN. Встановлює рівень ізоляції транзакцій для з'єднання значення Serializable.

**`PDO::SQLSRV_ENCODING_BINARY`**(int)

Визначає, що дані відправляються/виходять у вигляді потоку байтів до сервера без виконання перетворення кодування або іншого перетворення. Константа може бути передана функції PDOStatement::setAttribute, PDO::prepare, PDOStatement::bindColumn і PDOStatement::bindParam.

**`PDO::SQLSRV_ENCODING_SYSTEM`**(int)

Визначає, що дані відправляються/виходять до/від сервера в 8-бітному кодуванні локалі Windows, встановленої в системі. Усі мультибайтові символи та символи, що не перетворюються на це кодування, замінюються символом питання (?). Константа може бути передана до функцій PDOStatement::setAttribute, PDO::setAttribute, PDO::prepare, PDOStatement::bindColumn і PDOStatement::bindParam.

**`PDO::SQLSRV_ENCODING_UTF8`**(int)

Визначає, що дані відправляються/виходять до/від сервера в кодуванні UTF-8. Константа може бути передана до функцій PDOStatement::setAttribute, PDO::setAttribute, PDO::prepare, PDOStatement::bindColumn і PDOStatement::bindParam.

**`PDO::SQLSRV_ENCODING_DEFAULT`**(int)

Визначає, що дані відправляються/виходять до/від сервера відповідно до значення PDO::SQLSRV\_ENCODING\_SYSTEM, вказаному під час підключення. Для підключення може використовуватися кодування, вказане під час підготовки виразу. Константа може бути передана до функцій PDOStatement::setAttribute, PDO::setAttribute, PDO::prepare, PDOStatement::bindColumn і PDOStatement::bindParam.

**`PDO::SQLSRV_ATTR_QUERY_TIMEOUT`**(int)

Негативне ціле число, що відображає час очікування в секундах. Нуль (0) - це значення за промовчанням, що означає, що час очікування не враховується. Константа може бути передана функції PDOStatement::setAttribute, PDO::setAttribute і PDO::prepare.

**`PDO::SQLSRV_ATTR_DIRECT_QUERY`**(int)

Показує, що запит має бути негайно виконаний, без підготовки виразу. Константа може бути передана функції PDO::setAttribute і PDO::prepare. За подробицями зверніться до розділу документації [» Негайне виконання виразів та виконання підготовлених виразів](http://msdn.microsoft.com/en-us/library/ff754356.aspx)

## Зміст

-   [PDO\_SQLSRV DSN](ref.pdo-sqlsrv.connection.md)— Підключення до баз даних MS SQL Server та SQL Azure
