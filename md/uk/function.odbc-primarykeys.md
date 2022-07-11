- [«odbc_prepare](function.odbc-prepare.md)
- [odbc_procedurecolumns »](function.odbc-procedurecolumns.md)

- [PHP Manual](index.md)
- [Функції ODBC](ref.uodbc.md)
- Отримує первинні ключі таблиці

#odbc_primarykeys

(PHP 4, PHP 5, PHP 7, PHP 8)

odbc_primarykeys — Отримує первинні ключі таблиці

### Опис

**odbc_primarykeys**(
resource `$odbc`,
?string `$catalog`,
string `$schema`,
string `$table`
): resource \ | false

Повертає ідентифікатор результату, який можна використовувати для
отримання імен стовпців, що становлять первинний ключ таблиці.

### Список параметрів

`odbc`
Ідентифікатор з'єднання ODBC, за подробицями звертайтесь до
[odbc_connect()](function.odbc-connect.md).

`catalog`
Каталог ('qualifier' мовою ODBC 2).

`schema`
Схема ('owner' мовою ODBC 2).

`table`

### Значення, що повертаються

Повертає ідентифікатор результату ODBC або **`false`** у разі
виникнення помилки.

У результуючому наборі є такі стовпці:

- `TABLE_CAT`
- `TABLE_SCHEM`
- `TABLE_NAME`
- `COLUMN_NAME`
- `KEY_SEQ`
- `PK_NAME`

Драйвери можуть повідомляти додаткові стовпці.

Результуючий набір впорядковується за TABLE_CAT, TABLE_SCHEM,
`TABLE_NAME` та `KEY_SEQ`.

### Приклади

**Приклад #1 Перелік первинних ключів стовпця**

` <?php$conn==odbc_connect($dsn, $user, $pass);$primarykeys = odbc_primarykeys($conn, 'TutorialDB', 'dbo', 'TEST');while (($row =$ ))) {    print_r($row); break; // наступні рядки опущені для короткості}?> `

Результатом виконання цього прикладу буде щось подібне:

Array
(
[TABLE_CAT] => TutorialDB
[TABLE_SCHEM] => dbo
[TABLE_NAME] => TEST
[COLUMN_NAME] => id
[KEY_SEQ] => 1
[PK_NAME] => PK__TEST__3213E83FE141F843
)

### Дивіться також

- [odbc_tables()](function.odbc-tables.md) - Отримує список імен
таблиць, що зберігаються у певному джерелі даних
- [odbc_foreignkeys()](function.odbc-foreignkeys.md) - Повертає
список зовнішніх ключів
