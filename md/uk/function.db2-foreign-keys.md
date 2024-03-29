---
navigation:
  - function.db2-field-width.md: « db2\_field\_width
  - function.db2-free-result.md: db2\_free\_result »
  - index.md: PHP Manual
  - ref.ibm-db2.md: Функції IBM DB2
title: db2\_foreign\_keys
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# db2\_foreign\_keys

(PECL ibm\_db2 >= 1.0.0)

db2\_foreign\_keys — Повертає набір результатів, в якому перелічені ключі таблиці.

### Опис

```methodsynopsis
db2_foreign_keys(    resource $connection,    ?string $qualifier,    ?string $schema,    string $table_name): resource
```

Повертає набір результатів, де перелічені зовнішні ключі таблиці.

### Список параметрів

`connection`

Допустиме з'єднання з базою даних IBM DB2, Cloudscape або Apache Derby.

`qualifier`

Кваліфікатор баз даних DB2, що працюють на серверах OS/390 або z/OS. Для інших баз даних передайте **`null`** або порожній рядок.

`schema`

Схема містить таблиці. Якщо `schema` одно **`null`** **db2\_foreign\_keys()** відповідає схемою для поточного з'єднання.

`table_name`

Назва таблиці.

### Значення, що повертаються

Повертає ресурс оператора з набором результатів, що містить рядки, що описують зовнішні ключі зазначеної таблиці. Набір результатів складається з наступних стовпців:

| Название столбца | Опис |
| --- | --- |
| PKTABLE\_CAT | Назва каталогу таблиці, що містить первинний ключ. Значення NULL, якщо у цій таблиці немає каталогів. |
| PKTABLE\_SCHEM | Назва схеми таблиці, що містить первинний ключ. |
| PKTABLE\_NAME | Назва таблиці містить первинний ключ. |
| PKCOLUMN\_NAME | Назва стовпця, що містить первинний ключ. |
| FKTABLE\_CAT | Назва каталогу таблиці містить зовнішній ключ. Значення NULL, якщо у цій таблиці немає каталогів. |
| FKTABLE\_SCHEM | Назву схеми таблиці, що містить зовнішній ключ. |
| FKTABLE\_NAME | Назва таблиці містить зовнішній ключ. |
| FKCOLUMN\_NAME | Назва стовпця, що містить зовнішній ключ. |
| KEY\_SEQ | Індекс (починаючи з 1) стовпця у ключі. |
| UPDATE\_RULE | Цілочисленне значення, що представляє дію, що застосовується до зовнішнього ключа, якщо SQL - UPDATE. |
| DELETE\_RULE | Цілочисленне значення, що представляє дію, що застосовується до зовнішнього ключа, якщо операція SQL – DELETE. |
| FK\_NAME | Назва зовнішнього ключа. |
| PK\_NAME | Ім'я первинного ключа. |
| DEFERRABILITY | Цілочисленне значення, яке представляє, чи є можливість відстрочення зовнішнього ключа: SQL\_INITIALLY\_DEFERRED, SQL\_INITIALLY\_IMMEDIATE або SQL\_NOT\_DEFERRABLE. |

### Дивіться також

-   [db2\_column\_privileges()](function.db2-column-privileges.md) \- Повертає результуючий набір, що перераховує стовпці та пов'язані з ним привілеї для таблиці
-   [db2\_columns()](function.db2-columns.md) \- Повертає результуючий набір, що перераховує стовпці та пов'язані з ними метадані для таблиці
-   [db2\_primary\_keys()](function.db2-primary-keys.md) \- Повертає набір результатів, що містить первинні ключі таблиці
-   [db2\_procedure\_columns()](function.db2-procedure-columns.md) \- Повертає набір результатів зі списком параметрів процедури, що зберігається.
-   [db2\_procedures()](function.db2-procedures.md) \- Повертає набір результатів, в якому перераховані процедури, що зберігаються, зареєстровані в базі даних
-   [db2\_special\_columns()](function.db2-special-columns.md) \- Повертає набір результатів, у якому перераховані стовпці з унікальним ідентифікатором рядка таблиці
-   [db2\_statistics()](function.db2-statistics.md) \- Повертає набір результатів, що містить індекс та статистику таблиці
-   [db2\_table\_privileges()](function.db2-table-privileges.md) \- Повертає набір результатів, у якому перелічені таблиці та пов'язані з ними права доступу до бази даних
-   [db2\_tables()](function.db2-tables.md) \- Повертає набір результатів, у якому перелічені таблиці та пов'язані метадані в базі даних
