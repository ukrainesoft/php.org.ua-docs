---
navigation:
  - function.db2-table-privileges.md: « db2\_table\_privileges
  - set.mongodb.md: MongoDB »
  - index.md: PHP Manual
  - ref.ibm-db2.md: Функції IBM DB2
title: db2\_tables
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# db2\_tables

(PECL ibm\_db2 >= 1.0.0)

db2\_tables — Повертає набір результатів, у якому перелічені таблиці та пов'язані метадані в базі даних

### Опис

```methodsynopsis
db2_tables(    resource $connection,    ?string $qualifier = null,    ?string $schema = null,    ?string $table_name = null,    ?string $table_type = null): resource
```

Повертає набір результатів, у якому перелічені таблиці та пов'язані метадані у базі даних.

### Список параметрів

`connection`

Допустиме з'єднання з базою даних IBM DB2, Cloudscape або Apache Derby.

`qualifier`

Кваліфікатор баз даних DB2, що працюють на серверах OS/390 або z/OS. Для інших баз даних передайте **`null`** або порожній рядок.

`schema`

Схема містить таблиці. Параметр приймає шаблон пошуку, що містить `_`и`%` як підстановочні знаки.

`table_name`

Назва таблиці. Параметр приймає шаблон пошуку, що містить `_`и`%` як підстановочні знаки.

`table_type`

Список ідентифікаторів типів таблиць, розділених комами. Щоб відповідати всім типам таблиць, передайте **`null`** або порожній рядок. До допустимих ідентифікаторів типу таблиці відносяться: ALIAS, HIERARCHY TABLE, INOPERATIVE VIEW, NICKNAME, MATERIALIZED QUERY TABLE, SYSTEM TABLE, TABLE, TYPED TABLE, TYPED VIEW, та VIEW.

### Значення, що повертаються

Повертає ресурс виразу з набором результатів, що містить рядки, що описують таблиці, які відповідають зазначеним параметрам. Рядки складаються з наступних стовпців:

| Название столбца | Опис |
| --- | --- |
| TABLE\_CAT | Каталог, що містить таблицю або \*\*`null`\*\*якщо в цій таблиці немає каталогів. |
| TABLE\_SCHEM | Ім'я схеми, що містить таблицю. |
| TABLE\_NAME | Назва таблиці. |
| TABLE\_TYPE | Ідентифікатор типу таблиці. |
| REMARKS | Опис таблиці. |

### Дивіться також

-   [db2\_column\_privileges()](function.db2-column-privileges.md) \- Повертає результуючий набір, що перераховує стовпці та пов'язані з ним привілеї для таблиці
-   [db2\_columns()](function.db2-columns.md) \- Повертає результуючий набір, що перераховує стовпці та пов'язані з ними метадані для таблиці
-   [db2\_foreign\_keys()](function.db2-foreign-keys.md) \- Повертає набір результатів, у якому перелічені зовнішні ключі таблиці
-   [db2\_primary\_keys()](function.db2-primary-keys.md) \- Повертає набір результатів, що містить первинні ключі таблиці
-   [db2\_procedure\_columns()](function.db2-procedure-columns.md) \- Повертає набір результатів зі списком параметрів процедури, що зберігається.
-   [db2\_procedures()](function.db2-procedures.md) \- Повертає набір результатів, в якому перераховані процедури, що зберігаються, зареєстровані в базі даних
-   [db2\_special\_columns()](function.db2-special-columns.md) \- Повертає набір результатів, у якому перераховані стовпці з унікальним ідентифікатором рядка таблиці
-   [db2\_statistics()](function.db2-statistics.md) \- Повертає набір результатів, що містить індекс та статистику таблиці
-   [db2\_table\_privileges()](function.db2-table-privileges.md) \- Повертає набір результатів, у якому перелічені таблиці та пов'язані з ними права доступу до бази даних
