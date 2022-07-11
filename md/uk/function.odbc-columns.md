- [«odbc_columnprivileges](function.odbc-columnprivileges.md)
- [odbc_commit »](function.odbc-commit.md)

- [PHP Manual](index.md)
- [Функції ODBC](ref.uodbc.md)
- перераховує імена стовпців у зазначених таблицях

#odbc_columns

(PHP 4, PHP 5, PHP 7, PHP 8)

odbc_columns — Перелік імен стовпців у вказаних таблицях

### Опис

**odbc_columns**(
resource `$odbc`,
?string `$catalog` = **`null`**,
?string `$schema` = **`null`**,
?string `$table` = **`null`**,
?string `$column` = **`null`**
): resource \ | false

Перелічує усі стовпці у запитаному діапазоні.

### Список параметрів

`odbc`
Ідентифікатор з'єднання ODBC, за подробицями звертайтесь до
[odbc_connect()](function.odbc-connect.md).

`catalog`
Каталог ('qualifier' мовою ODBC 2).

`schema`
Схема ('owner' мовою ODBC 2). Цей параметр приймає такі
шаблони пошуку: `%` відповідний нулю або більше символів, та `_`
відповідний рівно одному символу.

`table`
Ім'я таблиці. Цей параметр приймає такі шаблони пошуку: `%`
відповідний нулю або більше символів, і `_` відповідний рівно
один символ.

`column`
Ім'я стовпця. Цей параметр приймає такі шаблони пошуку: `%`
відповідний нулю або більше символів, і `_` відповідний рівно
один символ.

### Значення, що повертаються

Повертає ідентифікатор результату ODBC або **`false`** у разі
виникнення помилки.

У результуючому наборі є такі стовпці:

- `TABLE_CAT`
- `TABLE_SCHEM`
- `TABLE_NAME`
- `COLUMN_NAME`
- `DATA_TYPE`
- `TYPE_NAME`
- `COLUMN_SIZE`
- `BUFFER_LENGTH`
- `DECIMAL_DIGITS`
- `NUM_PREC_RADIX`
- `NULLABLE`
- `REMARKS`
- `COLUMN_DEF`
- `SQL_DATA_TYPE`
- `SQL_DATETIME_SUB`
- `CHAR_OCTET_LENGTH`
- `ORDINAL_POSITION`
- `IS_NULLABLE`

Драйвери можуть повідомляти додаткові стовпці.

Результуючий набір впорядковується за TABLE_CAT, TABLE_SCHEM,
`TABLE_NAME` та `ORDINAL_POSITION`.

### Список змін

| Версія | Опис                                                    |
|--------|---------------------------------------------------------|
| 8.0.0  | schema, table та column тепер допускають значення null. |

### Приклади

**Приклад #1 Перелік стовпців таблиці**

` <?php$conn = odbc_connect($dsn, $user, $pass);$columns = odbc_columns($conn, 'TutorialDB', 'dbo', 'test', '%');while (($row = odbc_fetch_array($columns))) {    print_r($row); break; // наступні рядки опущені для короткості}?> `

Результатом виконання цього прикладу буде щось подібне:

Array
(
[TABLE_CAT] => TutorialDB
[TABLE_SCHEM] => dbo
[TABLE_NAME] => TEST
[COLUMN_NAME] => id
[DATA_TYPE] => 4
[TYPE_NAME] => int
[COLUMN_SIZE] => 10
[BUFFER_LENGTH] => 4
[DECIMAL_DIGITS] => 0
[NUM_PREC_RADIX] => 10
[NULLABLE] => 0
[REMARKS] =>
[COLUMN_DEF] =>
[SQL_DATA_TYPE] => 4
[SQL_DATETIME_SUB] =>
[CHAR_OCTET_LENGTH] =>
[ORDINAL_POSITION] => 1
[IS_NULLABLE] => NO
)

### Дивіться також

- [odbc_columnprivileges()](function.odbc-columnprivileges.md) -
Перелічує стовпці та пов'язані привілеї для даної таблиці
- [odbc_procedurecolumns()](function.odbc-procedurecolumns.md) -
Отримує інформацію про параметри процедур
