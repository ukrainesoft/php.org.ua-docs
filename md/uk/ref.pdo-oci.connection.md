---
navigation:
  - ref.pdo-oci.md: « Oracle (PDO)
  - ref.pdo-odbc.md: ODBC та DB2 (PDO) »
  - index.md: PHP Manual
  - ref.pdo-oci.md: Oracle (PDO)
title: PDO\_OCI DSN
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# PDO\_OCI DSN

(PECL PDO\_OCI >= 0.1.0)

PDO\_OCI DSN — З'єднання з базою даних Oracle

### Опис

Рядок підключення (Data Source Name, DSN) PDO\_OCI складається з наступних елементів:

Префікс DSN

**`oci:`**

`dbname`(Oracle Instant Client)

URI для Oracle Instant Client имеет вид`dbname=//hostname:port-number/database`. Якщо ви з'єднуєтеся з базою даних, вказаною в tnsnames.ora, ви можете використовувати тільки її ім'я: `dbname=database`

`charset`

Кодування за клієнта для заданого оточення.

### Приклади

**Приклад #1 Приклади використання PDO\_OCI DSN**

Наступні приклади показують з'єднання з базою даних Oracle:

```
// Соединение с базой данных, указанной в tnsnames.ora
oci:dbname=mydb

// Соединение с использованием Oracle Instant Client
oci:dbname=//localhost:1521/mydb
```
