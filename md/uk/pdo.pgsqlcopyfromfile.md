---
navigation:
  - pdo.pgsqlcopyfromarray.md: '« PDO::pgsqlCopyFromArray'
  - pdo.pgsqlcopytoarray.md: 'PDO::pgsqlCopyToArray »'
  - index.md: PHP Manual
  - ref.pdo-pgsql.md: PostgreSQL (PDO)
title: 'PDO::pgsqlCopyFromFile'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# PDO::pgsqlCopyFromFile

(PHP 5 >= 5.3.3, PHP 7, PHP 8)

PDO::pgsqlCopyFromFile — Скопіюйте дані з файлу до таблиці

### Опис

```methodsynopsis
public PDO::pgsqlCopyFromFile(    string $table_name,    string $filename,    string $delimiter = "\t",    string $null_as = "\\\\N",    string $fields = ?): bool
```

Копіює рядки з файлу `filename`в таблицу`table_name` використовуючи роздільник полів `delimiter` та список полів `fields`

### Список параметрів

`table_name`

Рядок з ім'ям таблиці

`filename`

Ім'я файлу з даними

`delimiter`

Розділювач полів, що використовується в `filename`

`null_as`

Як інтерпретувати значення NULL

`fields`

Список полів для вставки

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.
