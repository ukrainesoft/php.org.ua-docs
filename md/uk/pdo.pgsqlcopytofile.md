---
navigation:
  - pdo.pgsqlcopytoarray.md: '« PDO::pgsqlCopyToArray'
  - pdo.pgsqlgetnotify.md: 'PDO::pgsqlGetNotify »'
  - index.md: PHP Manual
  - ref.pdo-pgsql.md: PostgreSQL (PDO)
title: 'PDO::pgsqlCopyToFile'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# PDO::pgsqlCopyToFile

(PHP 5 >= 5.3.3, PHP 7, PHP 8)

PDO::pgsqlCopyToFile — Вивантаження таблиці у файл

### Опис

```methodsynopsis
public PDO::pgsqlCopyToFile(    string $table_name,    string $filename,    string $delimiter = "\t",    string $null_as = "\\\\N",    string $fields = ?): bool
```

Вивантажує дані у файл `filename` використовуючи роздільник полів `delimiter` та список полів `fields`

### Список параметрів

`table_name`

Рядок з ім'ям таблиці

`filename`

ім'я файлу

`delimiter`

Розділювач полів, що використовується в `filename`

`null_as`

Як інтерпретувати значення NULL

`fields`

Список полів для вставки

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.
