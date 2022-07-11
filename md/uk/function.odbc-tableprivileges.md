- [«odbc_statistics](function.odbc-statistics.md)
- [odbc_tables »](function.odbc-tables.md)

- [PHP Manual](index.md)
- [Функції ODBC](ref.uodbc.md)
- Перераховує таблиці та привілеї, пов'язані з кожною таблицею

#odbc_tableprivileges

(PHP 4, PHP 5, PHP 7, PHP 8)

odbc_tableprivileges — Перераховує таблиці та привілеї, пов'язані з
кожною таблицею

### Опис

**odbc_tableprivileges**(
resource `$odbc`,
?string `$catalog`,
string `$schema`,
string `$table`
): resource \ | false

Перелічує таблиці в запитаному діапазоні та привілеї, пов'язані з
кожною таблицею.

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

### Значення, що повертаються

Ідентифікатор результату ODBC або **`false`** у разі виникнення
помилки.

У результуючому наборі є такі стовпці:

- `TABLE_CAT`
- `TABLE_SCHEM`
- `TABLE_NAME`
- `GRANTOR`
- `GRANTEE`
- `PRIVILEGE`
- `IS_GRANTABLE`

Драйвери можуть повідомляти додаткові стовпці.

Результуючий набір впорядковується за TABLE_CAT, TABLE_SCHEM,
`TABLE_NAME`, `PRIVILEGE` та `GRANTEE`.

### Приклади

**Приклад #1 Перелік привілеїв таблиці**

` <?php$conn = odbc_connect($dsn, $user, $pass);$privileges = odbc_tableprivileges($conn, 'SalesOrders', 'dbo', 'Orders');while (($row =$ ))) {    print_r($row); break; // наступні рядки опущені для короткості}?> `

Результатом виконання цього прикладу буде щось подібне:

Array
(
[TABLE_CAT] => SalesOrders
[TABLE_SCHEM] => dbo
[TABLE_NAME] => Orders
[GRANTOR] => dbo
[GRANTEE] => dbo
[PRIVILEGE] => DELETE
[IS_GRANTABLE] => YES
)

### Дивіться також

- [odbc_tables()](function.odbc-tables.md) - Отримує список імен
таблиць, що зберігаються у певному джерелі даних
