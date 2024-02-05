---
navigation:
  - ref.pdo-sqlsrv.md: « MS SQL Server (PDO)
  - ref.pdo-oci.md: Oracle (PDO) »
  - index.md: PHP Manual
  - ref.pdo-sqlsrv.md: MS SQL Server (PDO)
title: PDO\_SQLSRV DSN
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# PDO\_SQLSRV DSN

(PECL pdo\_sqlsrv >= 2.0.1)

PDO\_SQLSRV DSN — Підключення до баз даних MS SQL Server та SQL Azure

### Опис

Рядок джерела даних (Data Source Name, DSN) для PDO\_SQLSRV складається з наступних елементів:

Префікс DSN

Префикс DSN равен\*\*`sqlsrv:`\*\*

`APP`

Ім'я програми, що використовується під час трасування.

`ConnectionPooling`

Визначає, чи береться з'єднання з пулу з'єднань (1 або **`true`**) чи ні (0 або **`false`**

`Database`

Назва бази даних.

`Encrypt`

Визначає, чи будуть шифруватись дані комунікації з SQL Server (1 або **`true`**) або не будуть (0 або **`false`**

`Failover_Partner`

Визначає сервер та екземпляр дзеркала бази даних (якщо включено та налаштовано) у разі недоступності первинного сервера.

`LoginTimeout`

Визначає час очікування на підключення (в секундах).

`MultipleActiveResultSets`

Вимикає або явно включає підтримку функції Multiple Active Result Sets (MARS) – повернення кількох результуючих наборів.

`QuotedId`

Визначає, використовувати для укладання в лапки ідентифікаторів стандарт SQL-92 (1 або **`true`**) або правила, що задаються Transact-SQL (0 або **`false`**

`Server`

Ім'я сервера бази даних.

`TraceFile`

Визначає шлях до файлу, який використовується для даних трасування.

`TraceOn`

Визначає, чи увімкнена для створюваного з'єднання функція трасування ODBC (1 або **`true`**) або відключена (0 або **`false`**

`TransactionIsolation`

Визначає рівень ізоляції транзакцій. Допустимі значення цієї опції - PDO::SQLSRV\_TXN\_READ\_UNCOMMITTED, PDO::SQLSRV\_TXN\_READ\_COMMITTED, PDO::SQLSRV\_TXN\_REPEATABLE\_READ, PDO::SQLSRV\_TXN\_SNAPSHOT та PDO::SQLSRV\_TXN\_SERIALIZABLE.

`TrustServerCertificate`

Определяет, должен ли клиент принимать (1 или\*\*`true`\*\*) або відхиляти (0 or **`false`**) самозавірені (self-signed) сертифікати сервера.

`WSID`

Визначає ім'я комп'ютера для трасування.

### Приклади

**Приклад #1 Приклади PDO\_SQLSRV DSN**

Наступний приклад показує, як підключатися до певної бази даних MS SQL Server:

```
$c = new PDO("sqlsrv:Server=localhost;Database=testdb", "UserName", "Password");
```

Наступний приклад показує, як підключатися до бази даних MS SQL Server за певним портом:

```
$c = new PDO("sqlsrv:Server=localhost,1521;Database=testdb", "UserName", "Password");
```

Наступний приклад показує, як підключатися до бази даних SQL Azure з ідентифікатором сервера 12345abcde. Примітка: при з'єднанні з SQL Azure за допомогою PDO ім'я користувача дорівнює UserName@12345abcde (UserName@ServerId).

```
$c = new PDO("sqlsrv:Server=12345abcde.database.windows.net;Database=testdb", "UserName@12345abcde", "Password");
```
