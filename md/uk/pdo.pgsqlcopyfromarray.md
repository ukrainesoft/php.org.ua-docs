Копіювати масив PHP до таблиці

-   [« PDO\_PGSQL DSN](ref.pdo-pgsql.connection.html)
    
-   [PDO::pgsqlCopyFromFile »](pdo.pgsqlcopyfromfile.html)
    
-   [PHP Manual](index.html)
    
-   [PostgreSQL (PDO)](ref.pdo-pgsql.html)
    
-   Копіювати масив PHP до таблиці
    

# PDO::pgsqlCopyFromArray

(PHP 5> = 5.3.3, PHP 7, PHP 8)

PDO::pgsqlCopyFromArray — Копіювати масив PHP до таблиці

### Опис

```methodsynopsis
public PDO::pgsqlCopyFromArray(    string $table_name,    array $rows,    string $delimiter = "\t",    string $null_as = "\\\\N",    string $fields = ?): bool
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