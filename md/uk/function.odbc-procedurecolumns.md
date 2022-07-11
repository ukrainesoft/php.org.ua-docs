- [«odbc_primarykeys](function.odbc-primarykeys.md)
- [odbc_procedures »](function.odbc-procedures.md)

- [PHP Manual](index.md)
- [Функції ODBC](ref.uodbc.md)
- Отримує інформацію про параметри процедур

#odbc_procedurecolumns

(PHP 4, PHP 5, PHP 7, PHP 8)

odbc_procedurecolumns — Отримує інформацію про параметри процедур

### Опис

**odbc_procedurecolumns**(
resource `$odbc`,
?string `$catalog` = **`null`**,
?string `$schema` = **`null`**,
?string `$procedure` = **`null`**,
?string `$column` = **`null`**
): resource \ | false

Отримує інформацію про параметри процедури.

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

`procedure`
Процедура. Цей параметр приймає такі шаблони пошуку: `%`
відповідний нулю або більше символів, і `_` відповідний рівно
один символ.

`column`
Стовпець. Цей параметр приймає такі шаблони пошуку: `%`
відповідний нулю або більше символів, і `_` відповідний рівно
один символ.

### Значення, що повертаються

Повертає список вхідних та вихідних параметрів, а також стовпці,
складові результуючий набір для зазначених процедур. Повертає
ідентифікатор результату ODBC або **`false`** у разі виникнення
помилки.

У результуючому наборі є такі стовпці:

- `PROCEDURE_CAT`
- `PROCEDURE_SCHEM`
- `PROCEDURE_NAME`
- `COLUMN_NAME`
- `COLUMN_TYPE`
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

Результуючий набір впорядковується за PROCEDURE_CAT,
`PROCEDURE_SCHEM`, `PROCEDURE_NAME` та `COLUMN_TYPE`.

### Список змін

| Версія | Опис                                                                              |
| ------ | --------------------------------------------------------------------------------- |
| 8.0.0  | До цієї версії функцію можна було викликати лише з одним або п'ятьма аргументами. |

### Приклади

**Приклад #1 Перелік стовпців процедури, що зберігається**

` <?php$conn = odbc_connect($dsn, $user, $pass);$columns = odbc_procedurecolumns($conn, 'TutorialDB', 'dbo', 'GetEmployeeSalesYTD;1', '%'); row==odbc_fetch_array($columns))) {   print_r($row); break; // наступні рядки опущені для короткості}?> `

Результатом виконання цього прикладу буде щось подібне:

Array
(
[PROCEDURE_CAT] => TutorialDB
[PROCEDURE_SCHEM] => dbo
[PROCEDURE_NAME] => GetEmployeeSalesYTD;1
[COLUMN_NAME] => @SalesPerson
[COLUMN_TYPE] => 1
[DATA_TYPE] => -9
[TYPE_NAME] => nvarchar
[COLUMN_SIZE] => 50
[BUFFER_LENGTH] => 100
[DECIMAL_DIGITS] =>
[NUM_PREC_RADIX] =>
[NULLABLE] => 1
[REMARKS] =>
[COLUMN_DEF] =>
[SQL_DATA_TYPE] => -9
[SQL_DATETIME_SUB] =>
[CHAR_OCTET_LENGTH] => 100
[ORDINAL_POSITION] => 1
[IS_NULLABLE] => YES
)

### Дивіться також

- [odbc_columns()](function.odbc-columns.md) - Перераховує імена
стовпців у зазначених таблицях
