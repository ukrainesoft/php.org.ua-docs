---
navigation:
  - ref.pdo-pgsql.connection.md: « PDOPGSQL DSN
  - pdo.pgsqlcopyfromfile.md: 'PDO::pgsqlCopyFromFile »'
  - index.md: PHP Manual
  - ref.pdo-pgsql.md: PostgreSQL (PDO)
title: 'PDO::pgsqlCopyFromArray'
---
# PDO::pgsqlCopyFromArray

(PHP 5> = 5.3.3, PHP 7, PHP 8)

PDO::pgsqlCopyFromArray — Копіювати масив PHP до таблиці

### Опис

```methodsynopsis
public PDO::pgsqlCopyFromArray(    string $table_name,    array $rows,    string $delimiter = "\t",    string $null_as = "\\\\N",    string $fields = ?): bool
```

Копіює дані з масиву `rows` до таблиці `table_name` з використанням роздільника полів `delimiter` та списку полів `fields`

### Список параметрів

`table_name`

Рядок з ім'ям таблиці

`rows`

Масив рядків із полями, розділеними `delimiter`

`delimiter`

Розділювач, що використовується в масиві `rows`

`null_as`

Як інтерпретувати значення NULL

`fields`

Список полів для вставки

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.
