- [«db2_primary_keys](function.db2-primary-keys.md)
- [db2_procedures »](function.db2-procedures.md)

- [PHP Manual](index.md)
- [Функції IBM DB2](ref.ibm-db2.md)
- Повертає набір результатів зі списком параметрів збереженої
процедури

#db2_procedure_columns

(PECL ibm_db2 \>= 1.0.0)

db2_procedure_columns — Повертає набір результатів зі списком
параметрів процедури, що зберігається

### Опис

**db2_procedure_columns**(
resource `$connection`,
string `$qualifier`,
string `$schema`,
string `$procedure`,
string `$parameter`
): resource

Повертає набір результатів, у якому перераховані параметри для однієї
або декількох процедур, що зберігаються.

### Список параметрів

`connection`
Допустиме з'єднання з базою даних IBM DB2, Cloudscape або Apache
Дербі.

`qualifier`
Кваліфікатор баз даних DB2, що працюють на серверах OS/390 або z/OS.
Для інших баз даних передайте **`null`** або порожній рядок.

`schema`
Схема містить процедури. Параметр приймає шаблон пошуку,
містить `_` і `%` як підстановочні знаки.

`procedure`
Назва процедури. Параметр приймає шаблон пошуку, що містить `_` і
`%` як підстановочні знаки.

`parameter`
Назва параметра. Параметр приймає шаблон пошуку, що містить `_` та `%` в
як підстановочні знаки. Якщо параметр дорівнює **`null`**,
повертаються всі параметри для зазначених процедур, що зберігаються.

### Значення, що повертаються

Повертає ресурс оператора з набором результатів, що містить рядки,
описуючі параметри для процедур, що зберігаються, відповідні зазначеним
параметрів. Рядки складаються з наступних стовпців:

[TABLE]

### Дивіться також

- [db2_column_privileges()](function.db2-column-privileges.md) -
Повертає результуючий набір, що перераховує стовпці та пов'язані з
ним привілеї для таблиці
- [db2_columns()](function.db2-columns.md) - Повертає
результуючий набір, що перераховує стовпці та пов'язані з ними
метадані для таблиці
- [db2_foreign_keys()](function.db2-foreign-keys.md) - Повертає
набір результатів, у якому перелічені зовнішні ключі таблиці
- [db2_primary_keys()](function.db2-primary-keys.md) - Повертає
набір результатів, що містить первинні ключі таблиці
- [db2_procedures()](function.db2-procedures.md) - Повертає набір
результатів, в якому перераховані процедури, що зберігаються,
зареєстровані у базі даних
- [db2_special_columns()](function.db2-special-columns.md) -
Повертає набір результатів, в якому перераховані стовпці з
унікальним ідентифікатором рядка таблиці
- [db2_statistics()](function.db2-statistics.md) - Повертає набір
результатів, що містить індекс та статистику таблиці
- [db2_table_privileges()](function.db2-table-privileges.md) -
Повертає набір результатів, у якому перераховані таблиці та
пов'язані з ними права доступу до бази даних
- [db2_tables()](function.db2-tables.md) - Повертає набір
результатів, в якому перераховані таблиці та пов'язані метадані в
базі даних
