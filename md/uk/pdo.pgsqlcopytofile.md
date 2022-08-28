Вивантаження таблиці у файл

-   [« PDO::pgsqlCopyToArray](pdo.pgsqlcopytoarray.html)
    
-   [PDO::pgsqlGetNotify »](pdo.pgsqlgetnotify.html)
    
-   [PHP Manual](index.html)
    
-   [PostgreSQL (PDO)](ref.pdo-pgsql.html)
    
-   Вивантаження таблиці у файл
    

# PDO::pgsqlCopyToFile

(PHP 5> = 5.3.3, PHP 7, PHP 8)

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

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.