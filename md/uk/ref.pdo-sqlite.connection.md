---
navigation:
  - ref.pdo-sqlite.md: « SQLite (PDO)
  - pdo.sqlitecreateaggregate.md: 'PDO::sqliteCreateAggregate »'
  - index.md: PHP Manual
  - ref.pdo-sqlite.md: SQLite (PDO)
title: PDO\_SQLITE DSN
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# PDO\_SQLITE DSN

(PHP 5 >= 5.1.0, PHP 7, PECL PDO\_SQLITE >= 0.2.0)

PDO\_SQLITE DSN — З'єднання з базою даних SQLite

### Опис

Ім'я джерела даних (Data Source Name, DSN) PDO\_SQLITE складається з наступних елементів:

DSN-префікс (SQLite 3)

DSN-префікс - це **`sqlite:`**

-   Для доступу до бази даних на диску абсолютний шлях повинен бути доданий до DSN-префіксу.
    
-   Для створення бази даних у пам'яті,`:memory:`має бути доданий до DSN-префіксу.
    
-   Якщо DSN складається лише з префіксу DSN, використовується тимчасова база даних, яка видаляється при закритті з'єднання.
    

### Приклади

**Приклад #1 Приклад DSN PDO\_SQLITE**

У наступному прикладі показано DSN PDO\_SQLITE для з'єднання з SQLite:

```
sqlite:/opt/databases/mydb.sq3
sqlite::memory:
sqlite:
```
