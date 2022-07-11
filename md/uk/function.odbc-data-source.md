- [«odbc_cursor](function.odbc-cursor.md)
- [odbc_do »](function.odbc-do.md)

- [PHP Manual](index.md)
- [Функції ODBC](ref.uodbc.md)
- Повертає інформацію про доступні DSN

#odbc_data_source

(PHP 4 \>= 4.3.0, PHP 5, PHP 7, PHP 8)

odbc_data_source — Повертає інформацію про доступні DSN

### Опис

**odbc_data_source**(resource `$odbc`, int `$fetch_type`): array\|false

Ця функція поверне список доступних DSN (після кількох дзвінків).

### Список параметрів

`odbc`
Ідентифікатор з'єднання ODBC, за подробицями звертайтесь до
[odbc_connect()](function.odbc-connect.md).

`fetch_type`
`fetch_type` може бути одним із двох типів констант:
**`SQL_FETCH_FIRST`**, **`SQL_FETCH_NEXT`**. Використовуйте
**`SQL_FETCH_FIRST`** при першому виклику цієї функції, після цього
використовуйте **`SQL_FETCH_NEXT`**.

### Значення, що повертаються

Повертає **`false`** у разі виникнення помилки, масив (array) у
у разі успішного виконання та **`null`** після вибірки останнього
доступного DSN.

### Приклади

**Приклад #1 Перелік доступних DSN**

` <?php$conn==odbc_connect('dsn', 'user', 'pass');$dsn_info = odbc_data_source($conn, SQL_FETCH_FIRST);while ($dsn_info) {     $dsn_info==odbc_data_source($conn, SQL_FETCH_NEXT);}?> `

Результатом виконання цього прикладу буде щось подібне:

Array
(
[server] => dsn
[description] => ODBC Driver 17 for SQL Server
)
Array
(
[server] => other_dsn
[description] => Microsoft Access Driver (*.mdb, *.accdb)
)
