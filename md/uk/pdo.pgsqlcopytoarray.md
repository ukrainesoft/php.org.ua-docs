Вивантажити дані з таблиці до масиву PHP

-   [« PDO::pgsqlCopyFromFile](pdo.pgsqlcopyfromfile.html)
    
-   [PDO::pgsqlCopyToFile »](pdo.pgsqlcopytofile.html)
    
-   [PHP Manual](index.html)
    
-   [PostgreSQL (PDO)](ref.pdo-pgsql.html)
    
-   Вивантажити дані з таблиці до масиву PHP
    

# PDO::pgsqlCopyToArray

(PHP 5> = 5.3.3, PHP 7, PHP 8)

PDO::pgsqlCopyToArray — Вивантажити дані з таблиці до масиву PHP

### Опис

```methodsynopsis
public PDO::pgsqlCopyToArray(    string $table_name,    string $delimiter = "\t",    string $null_as = "\\\\N",    string $fields = ?): array|false
```

Вивантажує дані з таблиці `table` в масив, використовуючи роздільник `delimiter` та список полів `fields`

### Список параметрів

`table_name`

Рядок з ім'ям таблиці

`delimiter`

Роздільник полів

`null_as`

Як інтерпретувати значення NULL

`fields`

Список полів для вставки

### Значення, що повертаються

Повертає масив рядків або **`false`** у разі виникнення помилки.