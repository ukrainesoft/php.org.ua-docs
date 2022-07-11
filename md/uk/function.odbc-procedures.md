- [«odbc_procedurecolumns](function.odbc-procedurecolumns.md)
- [odbc_result_all »](function.odbc-result-all.md)

- [PHP Manual](index.md)
- [Функції ODBC](ref.uodbc.md)
- Отримує список процедур, що зберігаються у певному джерелі даних

#odbc_procedures

(PHP 4, PHP 5, PHP 7, PHP 8)

odbc_procedures — Отримує список процедур, що зберігаються у певному
джерелі даних

### Опис

**odbc_procedures**(
resource `$odbc`,
?string `$catalog` = **`null`**,
?string `$schema` = **`null`**,
?string `$procedure` = **`null`**
): resource \ | false

Перелічує всі процедури в діапазоні.

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
Ім'я процедури. Цей параметр приймає такі шаблони пошуку: `%`
відповідний нулю або більше символів, і `_` відповідний рівно
один символ.

### Значення, що повертаються

Повертає ідентифікатор результату ODBC, який містить інформацію або
**`false`** у разі виникнення помилки.

У результуючому наборі є такі стовпці:

- `PROCEDURE_CAT`
- `PROCEDURE_SCHEM`
- `PROCEDURE_NAME`
- `NUM_INPUT_PARAMS`
- `NUM_OUTPUT_PARAMS`
- `NUM_RESULT_SETS`
- `REMARKS`
- `PROCEDURE_TYPE`

Драйвери можуть повідомляти додаткові стовпці.

Результуючий набір впорядковується за PROCEDURE_CAT,
`PROCEDURE_SCHEMA` та `PROCEDURE_NAME`.

### Список змін

| Версія | Опис                                                                              |
| ------ | --------------------------------------------------------------------------------- |
| 8.0.0  | До цієї версії функцію можна було викликати лише з одним або чотирма аргументами. |

### Приклади

**Приклад #1 Перелік процедур бази даних**

` <?php$conn==odbc_connect($dsn, $user, $pass);$procedures = odbc_procedures($conn, $catalog, $schema, '%');while(($row = odbc_fetch_arra ) {    print_r($row); break; // наступні рядки опущені для короткості}?> `

Результатом виконання цього прикладу буде щось подібне:

Array
(
[PROCEDURE_CAT] => TutorialDB
[PROCEDURE_SCHEM] => dbo
[PROCEDURE_NAME] => GetEmployeeSalesYTD;1
[NUM_INPUT_PARAMS] => -1
[NUM_OUTPUT_PARAMS] => -1
[NUM_RESULT_SETS] => -1
[REMARKS] =>
[PROCEDURE_TYPE] => 2
)

### Дивіться також

- [odbc_procedurecolumns()](function.odbc-procedurecolumns.md) -
Отримує інформацію про параметри процедур
- [odbc_tables()](function.odbc-tables.md) - Отримує список імен
таблиць, що зберігаються у певному джерелі даних
