- [«odbc_close](function.odbc-close.md)
- [odbc_columns »](function.odbc-columns.md)

- [PHP Manual](index.md)
- [Функції ODBC](ref.uodbc.md)
- Перераховує стовпці та пов'язані привілеї для даної таблиці

#odbc_columnprivileges

(PHP 4, PHP 5, PHP 7, PHP 8)

odbc_columnprivileges — Перераховує стовпці та пов'язані привілеї для
даної таблиці

### Опис

**odbc_columnprivileges**(
resource `$odbc`,
?string `$catalog`,
string `$schema`,
string `$table`,
string `$column`
): resource \ | false

Перераховує стовпці та пов'язані привілеї для даної таблиці.

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
виникнення помилки. Цей ідентифікатор результату можна використовувати
для отримання списку стовпців та пов'язаних привілеїв.

У результуючому наборі є такі стовпці:

- `TABLE_CAT`
- `TABLE_SCHEM`
- `TABLE_NAME`
- `COLUMN_NAME`
- `GRANTOR`
- `GRANTEE`
- `PRIVILEGE`
- `IS_GRANTABLE`

Драйвери можуть повідомляти додаткові стовпці.

Результуючий набір впорядковується за TABLE_CAT, TABLE_SCHEM,
`TABLE_NAME`, `COLUMN_NAME` та `PRIVILEGE`.

### Приклади

**Приклад #1 Перелік привілеїв для стовпця**

` <?php$conn = odbc_connect($dsn, $user, $pass);$privileges = odbc_columnprivileges($conn, 'TutorialDB', 'dbo', 'test', 'id');while (($row odbc_fetch_array($privileges))) {    print_r($row); break; // наступні рядки опущені для короткості}?> `

Результатом виконання цього прикладу буде щось подібне:

Array
(
[TABLE_CAT] => TutorialDB
[TABLE_SCHEM] => dbo
[TABLE_NAME] => test
[COLUMN_NAME] => id
[GRANTOR] => dbo
[GRANTEE] => dbo
[PRIVILEGE] => INSERT
[IS_GRANTABLE] => YES
)
