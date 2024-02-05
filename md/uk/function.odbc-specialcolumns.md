---
navigation:
  - function.odbc-setoption.md: « odbc\_setoption
  - function.odbc-statistics.md: odbc\_statistics »
  - index.md: PHP Manual
  - ref.uodbc.md: Функції ODBC
title: odbc\_specialcolumns
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# odbc\_specialcolumns

(PHP 4, PHP 5, PHP 7, PHP 8)

odbc\_specialcolumns — Витягує спеціальні стовпці

### Опис

```methodsynopsis
odbc_specialcolumns(    resource $odbc,    int $type,    ?string $catalog,    string $schema,    string $table,    int $scope,    int $nullable): resource|false
```

Витягує або оптимальний набір стовпців, який однозначно визначає рядок у таблиці, або стовпці, які автоматично оновлюються, коли будь-яке значення у рядку оновлюється транзакцією.

### Список параметрів

`odbc`

Ідентифікатор з'єднання ODBC, за подробицями звертайтесь до [odbc\_connect()](function.odbc-connect.md)

`type`

Когда аргументом является\*\*`SQL_BEST_ROWID`\*\* **odbc\_specialcolumns()** повертає стовпець чи стовпці, які однозначно ідентифікують кожен рядок у таблиці. Коли аргументом є **`SQL_ROWVER`** **odbc\_specialcolumns()** повертає стовпець або стовпці у зазначеній таблиці, якщо вони є, які автоматично оновлюються джерелом даних, коли будь-яке значення у рядку оновлюється будь-якою транзакцією.

`catalog`

Каталог ('qualifier' мовою ODBC 2).

`schema`

Схема ('owner' мовою ODBC 2).

`table`

Таблиця.

`scope`

Область, яка впорядковує результуючий набір. Одна з констант **`SQL_SCOPE_CURROW`** **`SQL_SCOPE_TRANSACTION`** або **`SQL_SCOPE_SESSION`**

`nullable`

Визначає, чи повертати спеціальні стовпці, які можуть мати значення NULL. Одна з констант **`SQL_NO_NULLS`** або **`SQL_NULLABLE`**

### Значення, що повертаються

Повертає ідентифікатор результату ODBC або \*\*`false`\*\*в случае возникновения ошибки.

У результуючому наборі є такі стовпці:

-   `SCOPE`
-   `COLUMN_NAME`
-   `DATA_TYPE`
-   `TYPE_NAME`
-   `COLUMN_SIZE`
-   `BUFFER_LENGTH`
-   `DECIMAL_DIGITS`
-   `PSEUDO_COLUMN`

Драйвери можуть повідомляти додаткові стовпці.

Результирующий набор упорядочивается по`SCOPE`

### Дивіться також

-   [odbc\_tables()](function.odbc-tables.md) \- Отримує список імен таблиць, що зберігаються у певному джерелі даних
