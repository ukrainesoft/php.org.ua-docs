---
navigation:
  - function.db2-table-privileges.md: « db2tableprivileges
  - set.mongodb.md: MongoDB »
  - index.md: PHP Manual
  - ref.ibm-db2.md: Функції IBM DB2
title: db2tables
---
# db2tables

(PECL ibmdb2> = 1.0.0)

db2tables — Повертає набір результатів, у якому перелічені таблиці та пов'язані метадані в базі даних

### Опис

```methodsynopsis
db2_tables(    resource $connection,    string $qualifier = ?,    string $schema = ?,    string $table-name = ?,    string $table-type = ?): resource
```

Повертає набір результатів, у якому перелічені таблиці та пов'язані метадані у базі даних.

### Список параметрів

`connection`

Допустиме з'єднання з базою даних IBM DB2, Cloudscape або Apache Derby.

`qualifier`

Кваліфікатор баз даних DB2, що працюють на серверах OS/390 або z/OS. Для інших баз даних передайте **`null`** або порожній рядок.

`schema`

Схема містить таблиці. Параметр приймає шаблон пошуку, що містить `_` і `%` як підстановочні знаки.

`table-name`

Назва таблиці. Параметр приймає шаблон пошуку, що містить `_` і `%` як підстановочні знаки.

`table-type`

Список ідентифікаторів типів таблиць, розділених комами. Щоб відповідати всім типам таблиць, передайте **`null`** або порожній рядок. До допустимих ідентифікаторів типу таблиці відносяться: ALIAS, HIERARCHY TABLE, INOPERATIVE VIEW, NICKNAME, MATERIALIZED QUERY TABLE, SYSTEM TABLE, TABLE, TYPED TABLE, TYPED VIEW, та VIEW.

### Значення, що повертаються

Повертає ресурс виразу з набором результатів, що містить рядки, що описують таблиці, які відповідають зазначеним параметрам. Рядки складаються з наступних стовпців:

| Название столбца | Описание |
| --- | --- |
| TABLECAT | Каталог, що містить таблицю або \*\*`null`\*\*якщо в цій таблиці немає каталогів. |
| TABLESCHEM | Ім'я схеми, що містить таблицю. |
| TABLENAME | Назва таблиці. |
| TABLETYPE | Ідентифікатор типу таблиці. |
| REMARKS | Опис таблиці. |

### Дивіться також

-   [db2columnprivileges()](function.db2-column-privileges.md) - Повертає результуючий набір, що перераховує стовпці та пов'язані з ним привілеї для таблиці
-   [db2columns()](function.db2-columns.md) - Повертає результуючий набір, що перераховує стовпці та пов'язані з ними метадані для таблиці
-   [db2foreignkeys()](function.db2-foreign-keys.md) - Повертає набір результатів, у якому перелічені зовнішні ключі таблиці
-   [db2primarykeys()](function.db2-primary-keys.md) - Повертає набір результатів, що містить первинні ключі таблиці
-   [db2procedurecolumns()](function.db2-procedure-columns.md) - Повертає набір результатів зі списком параметрів процедури, що зберігається.
-   [db2procedures()](function.db2-procedures.md) - Повертає набір результатів, в якому перераховані процедури, що зберігаються, зареєстровані в базі даних
-   [db2specialcolumns()](function.db2-special-columns.md) - Повертає набір результатів, у якому перераховані стовпці з унікальним ідентифікатором рядка таблиці
-   [db2statistics()](function.db2-statistics.md) - Повертає набір результатів, що містить індекс та статистику таблиці
-   [db2tableprivileges()](function.db2-table-privileges.md) - Повертає набір результатів, у якому перелічені таблиці та пов'язані з ними права доступу до бази даних
