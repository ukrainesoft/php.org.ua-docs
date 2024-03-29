---
navigation:
  - function.db2-prepare.md: « db2\_prepare
  - function.db2-procedure-columns.md: db2\_procedure\_columns »
  - index.md: PHP Manual
  - ref.ibm-db2.md: Функції IBM DB2
title: db2\_primary\_keys
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# db2\_primary\_keys

(PECL ibm\_db2 >= 1.0.0)

db2\_primary\_keys — Повертає набір результатів, що містить первинні ключі таблиці

### Опис

```methodsynopsis
db2_primary_keys(    resource $connection,    ?string $qualifier,    ?string $schema,    string $table_name): resource
```

Повертає набір результатів, що містить первинні ключі таблиці.

### Список параметрів

`connection`

Допустиме з'єднання з базою даних IBM DB2, Cloudscape або Apache Derby.

`qualifier`

Кваліфікатор баз даних DB2, що працюють на серверах OS/390 або z/OS. Для інших баз даних передайте **`null`** або порожній рядок.

`schema`

Схема містить таблиці. Якщо `schema`равен\*\*`null`\*\* **db2\_primary\_keys()** відповідає схемою для поточного з'єднання.

`table_name`

Назва таблиці.

### Значення, що повертаються

Повертає ресурс оператора з набором результатів, що містить рядки, що описують первинні ключі зазначеної таблиці. Набір результатів складається з наступних стовпців:

| Название столбца | Опис |
| --- | --- |
| TABLE\_CAT | Назва каталогу таблиці, що містить первинний ключ. Значення NULL, якщо у цій таблиці немає каталогів. |
| TABLE\_SCHEM | Назва схеми таблиці, що містить первинний ключ. |
| TABLE\_NAME | Назва таблиці містить первинний ключ. |
| COLUMN\_NAME | Назва стовпця, що містить первинний ключ. |
| KEY\_SEQ | Індекс стовпця (починаючи з 1) у ключі. |
| PK\_NAME | Ім'я первинного ключа. |

### Дивіться також

-   [db2\_column\_privileges()](function.db2-column-privileges.md) \- Повертає результуючий набір, що перераховує стовпці та пов'язані з ним привілеї для таблиці
-   [db2\_columns()](function.db2-columns.md) \- Повертає результуючий набір, що перераховує стовпці та пов'язані з ними метадані для таблиці
-   [db2\_foreign\_keys()](function.db2-foreign-keys.md) \- Повертає набір результатів, у якому перелічені зовнішні ключі таблиці
-   [db2\_procedure\_columns()](function.db2-procedure-columns.md) \- Повертає набір результатів зі списком параметрів процедури, що зберігається.
-   [db2\_procedures()](function.db2-procedures.md) \- Повертає набір результатів, в якому перераховані процедури, що зберігаються, зареєстровані в базі даних
-   [db2\_special\_columns()](function.db2-special-columns.md) \- Повертає набір результатів, у якому перераховані стовпці з унікальним ідентифікатором рядка таблиці
-   [db2\_statistics()](function.db2-statistics.md) \- Повертає набір результатів, що містить індекс та статистику таблиці
-   [db2\_table\_privileges()](function.db2-table-privileges.md) \- Повертає набір результатів, у якому перелічені таблиці та пов'язані з ними права доступу до бази даних
-   [db2\_tables()](function.db2-tables.md) \- Повертає набір результатів, у якому перелічені таблиці та пов'язані метадані в базі даних
