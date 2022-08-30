Функції модуля PDOSQLSRV для Microsoft SQL Server

-   [« PDOMYSQL DSN](ref.pdo-mysql.connection.html)
    
-   [PDOSQLSRV DSN »](ref.pdo-sqlsrv.connection.html)
    
-   [PHP Manual](index.html)
    
-   [Драйвери PDO](pdo.drivers.html)
    
-   Функції модуля PDOSQLSRV для Microsoft SQL Server
    

# Функції модуля PDOSQLSRV для Microsoft SQL Server

## Вступ

PDOSQLSRV - це драйвер, що реалізує інтерфейс [PHP Data Objects (PDO)](intro.pdo.html) для отримання доступу з PHP до баз даних MS SQL Server (починаючи з версії SQL Server 2005) та SQL Azure.

## Встановлення

Модуль PDOSQLSRV включається додаванням відповідного файлу DLL в директорію модулів вашої встановленої копії PHP і відповідного запису файл php.ini. Завантажена копія модуля PDOSQLSRV включає вісім файлів драйверів, чотири з них для підтримки PDO.

Найчастіше використовувана версія драйвера доступна тут: [» Загрузка SQLSRV](http://msdn.microsoft.com/en-us/sqlserver/ff657782.aspx). Вихідний код драйвера розміщено в [» публічній репозиторії](https://github.com/microsoft/msphpsql)

За детальною інформацією про системні вимоги зверніться до розділу [» Системні вимоги SQLSRV](http://msdn.microsoft.com/en-us/library/cc296170.aspx)

Модуль PDOSQLSRV може використовуватися з PHP лише у Windows. Для Linux використовуйте [ODBC](ref.pdo-odbc.html) і [» Microsoft's SQL Server ODBC Driver для Linux](http://www.microsoft.com/download/en/details.aspx?id=28160)

## Обумовлені константи

Наведені нижче константи визначені цим драйвером і будуть доступні лише у випадку, якщо PHP був зібраний з підтримкою цього модуля, або цей модуль був динамічно завантажений під час виконання. Крім того, ці залежні від драйвера константи повинні бути використані лише разом із цим драйвером. Використання атрибутів, специфічних для деякого драйвера з іншим драйвером, може викликати несподівану поведінку. Якщо ваш код виконується з кількома драйверами, можна використовувати функцію [PDO::getAttribute()](pdo.getattribute.html) для отримання атрибуту **`PDO::ATTR_DRIVER_NAME`** для перевірки драйвера.

**`PDO::SQLSRV_TXN_READ_UNCOMMITTED`** (int)

Ця константа - допустиме значення для ключа TransactionIsolation SQLSRV DSN. Встановлює рівень ізоляції транзакцій для з'єднання значення Read Uncommitted.

**`PDO::SQLSRV_TXN_READ_COMMITTED`** (int)

Ця константа - допустиме значення для ключа TransactionIsolation SQLSRV DSN. Встановлює рівень ізоляції транзакцій для з'єднання значення Read Committed.

**`PDO::SQLSRV_TXN_REPEATABLE_READ`** (int)

Ця константа - допустиме значення для ключа TransactionIsolation SQLSRV DSN. Встановлює рівень ізоляції транзакцій для з'єднання значення Repeateable Read.

**`PDO::SQLSRV_TXN_SNAPSHOT`** (int)

Ця константа - допустиме значення для ключа TransactionIsolation SQLSRV DSN. Встановлює рівень ізоляції транзакцій для з'єднання значення Snapshot.

**`PDO::SQLSRV_TXN_SERIALIZABLE`** (int)

Ця константа - допустиме значення для ключа TransactionIsolation SQLSRV DSN. Встановлює рівень ізоляції транзакцій для з'єднання значення Serializable.

**`PDO::SQLSRV_ENCODING_BINARY`** (int)

Визначає, що дані відправляються/виходять у вигляді потоку байтів до сервера без виконання перетворення кодування або іншого перетворення. Константа може бути передана функції PDOStatement::setAttribute, PDO::prepare, PDOStatement::bindColumn і PDOStatement::bindParam.

**`PDO::SQLSRV_ENCODING_SYSTEM`** (int)

Визначає, що дані відправляються/виходять до/від сервера в 8-бітному кодуванні локалі Windows, встановленої в системі. Усі мультибайтові символи та символи, що не перетворюються на це кодування, замінюються символом питання (?). Константа може бути передана до функцій PDOStatement::setAttribute, PDO::setAttribute, PDO::prepare, PDOStatement::bindColumn і PDOStatement::bindParam.

**`PDO::SQLSRV_ENCODING_UTF8`** (int)

Визначає, що дані відправляються/виходять до/від сервера в кодуванні UTF-8. Константа може бути передана до функцій PDOStatement::setAttribute, PDO::setAttribute, PDO::prepare, PDOStatement::bindColumn і PDOStatement::bindParam.

**`PDO::SQLSRV_ENCODING_DEFAULT`** (int)

Визначає, що дані відправляються/виходять до/від сервера відповідно до значення PDO::SQLSRVENCODINGSYSTEM, вказаному під час підключення. Для підключення може використовуватися кодування, вказане під час підготовки виразу. Константа може бути передана до функцій PDOStatement::setAttribute, PDO::setAttribute, PDO::prepare, PDOStatement::bindColumn і PDOStatement::bindParam.

**`PDO::SQLSRV_ATTR_QUERY_TIMEOUT`** (int)

Негативне ціле число, що відображає час очікування в секундах. Нуль (0) - це значення за промовчанням, що означає, що час очікування не враховується. Константа може бути передана функції PDOStatement::setAttribute, PDO::setAttribute і PDO::prepare.

**`PDO::SQLSRV_ATTR_DIRECT_QUERY`** (int)

Показує, що запит має бути негайно виконаний, без підготовки виразу. Константа може бути передана функції PDO::setAttribute і PDO::prepare. За подробицями зверніться до розділу документації [» Немедленное выполнение выражений и выполнение подготовленных выражений](http://msdn.microsoft.com/en-us/library/ff754356.aspx)

## Зміст

-   [PDOSQLSRV DSN](ref.pdo-sqlsrv.connection.html) — Підключення до баз даних MS SQL Server та SQL Azure