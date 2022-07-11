- [MS SQL Server (PDO)](ref.pdo-sqlsrv.md)
- [Oracle (PDO) »](ref.pdo-oci.md)

- [PHP Manual](index.md)
- [MS SQL Server (PDO)](ref.pdo-sqlsrv.md)
- Підключення до баз даних MS SQL Server та SQL Azure

#PDO_SQLSRV DSN

(PECL pdo_sqlsrv \>= 2.0.1)

PDO_SQLSRV DSN — Підключення до баз даних MS SQL Server та SQL Azure

### Опис

Рядок джерела даних (Data Source Name, DSN) для PDO_SQLSRV складається
з наступних елементів:

Префікс DSN
Префікс DSN дорівнює **`sqlsrv:`**.

`APP`
Ім'я програми, що використовується під час трасування.

`ConnectionPooling`
Визначає, чи береться з'єднання з пулу з'єднань (1 або **`true`**)
чи ні (0 або **`false`**).

`Database`
Назва бази даних.

`Encrypt`
Визначає, чи будуть шифруватися дані комунікації з SQL Server (1 або
**`true`**) або не будуть (0 або **`false`**).

`Failover_Partner`
Визначає сервер та екземпляр дзеркала бази даних (якщо включено та
настроєно) у разі недоступності первинного сервера.

`LoginTimeout`
Визначає час очікування на підключення (в секундах).

`MultipleActiveResultSets`
Вимикає або явно вмикає підтримку функції Multiple Active Result
Sets (MARS) – повернення кількох результуючих наборів.

`QuotedId`
Визначає, використовувати для укладання в лапки ідентифікаторів
стандарт SQL-92 (1 або **`true`**) або правила, що задаються Transact-SQL
(0 або **`false`**).

`Server`
Ім'я сервера бази даних.

`TraceFile`
Визначає шлях до файлу, який використовується для даних трасування.

`TraceOn`
Визначає, чи включена для створюваного з'єднання функція трасування
ODBC (1 або **`true`**) або відключена (0 або **`false`**).

TransactionIsolation
Визначає рівень ізоляції транзакцій. Допустимі значення даної
опції - PDO::SQLSRV_TXN_READ_UNCOMMITTED,
PDO::SQLSRV_TXN_READ_COMMITTED, PDO::SQLSRV_TXN_REPEATABLE_READ,
PDO::SQLSRV_TXN_SNAPSHOT та PDO::SQLSRV_TXN_SERIALIZABLE.

`TrustServerCertificate`
Визначає, чи клієнт повинен приймати (1 або **`true`**) або відхиляти
(0 or **`false`**) самозавірені (self-signed) сертифікати сервера.

`WSID`
Визначає ім'я комп'ютера для трасування.

### Приклади

**Приклад #1 Приклади PDO_SQLSRV DSN**

Наступний приклад показує, як підключатися до певної бази даних
MS SQL Server:

$c = new PDO("sqlsrv:Server=localhost;Database=testdb", "UserName", "Password");

Наступний приклад показує, як підключатися до бази даних MS SQL
Server по певному порту:

$c = новий PDO("sqlsrv:Server=localhost,1521;Database=testdb", "UserName", "Password");

Наступний приклад показує, як підключатися до бази даних SQL Azure з
ідентифікатор сервера 12345abcde. Примітка: при підключенні до SQL
Azure за допомогою PDO, ім'я користувача дорівнює UserName@12345abcde
(UserName@ServerId).

$c = new PDO("sqlsrv:Server=12345abcde.database.windows.net;Database=testdb", "UserName@12345abcde", "Password");
