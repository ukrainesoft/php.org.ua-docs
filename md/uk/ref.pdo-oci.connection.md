З'єднання з базою даних Oracle

-   [« Oracle (PDO)](ref.pdo-oci.html)
    
-   [ODBC и DB2 (PDO) »](ref.pdo-odbc.html)
    
-   [PHP Manual](index.html)
    
-   [Oracle (PDO)](ref.pdo-oci.html)
    
-   З'єднання з базою даних Oracle
    

# PDOOCI DSN

(PECL PDOOCI> = 0.1.0)

PDOOCI DSN — З'єднання з базою даних Oracle

### Опис

Рядок підключення (Data Source Name, DSN) PDOOCI складається з наступних елементів:

Префікс DSN

**`oci:`**

`dbname` (Oracle Instant Client)

URI для Oracle Instant Client має вигляд `dbname=//hostname:port-number/database`. Якщо ви з'єднуєтеся з базою даних, вказаною в tnsnames.ora, ви можете використовувати тільки її ім'я: `dbname=database`

`charset`

Кодування за клієнта для заданого оточення.

### Приклади

**Приклад #1 Приклади використання PDOOCI DSN**

Наступні приклади показують з'єднання з базою даних Oracle:

```
// Соединение с базой данных, указанной в tnsnames.ora
oci:dbname=mydb

// Соединение с использованием Oracle Instant Client
oci:dbname=//localhost:1521/mydb
```