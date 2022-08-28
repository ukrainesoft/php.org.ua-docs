З'єднання з базою даних SQLite

-   [« SQLite (PDO)](ref.pdo-sqlite.html)
    
-   [PDO::sqliteCreateAggregate »](pdo.sqlitecreateaggregate.html)
    
-   [PHP Manual](index.html)
    
-   [SQLite (PDO)](ref.pdo-sqlite.html)
    
-   З'єднання з базою даних SQLite
    

# PDOSQLITE DSN

(PHP 5> = 5.1.0, PHP 7, PECL PDOSQLITE> = 0.2.0)

PDOSQLITE DSN — З'єднання з базою даних SQLite

### Опис

Ім'я джерела даних (Data Source Name, DSN) PDOSQLITE складається з наступних елементів:

DSN-префікс (SQLite 3)

DSN-префікс - це **`sqlite:`**

-   Для доступу до бази даних на диску абсолютний шлях повинен бути доданий до DSN-префіксу.
    
-   Для створення бази даних у пам'яті, `:memory:` має бути доданий до DSN-префіксу.
    
-   Якщо DSN складається лише з префіксу DSN, використовується тимчасова база даних, яка видаляється при закритті з'єднання.
    

### Приклади

**Приклад #1 Приклад DSN PDOSQLITE**

У наступному прикладі показано DSN PDOSQLITE для з'єднання з SQLite:

```
sqlite:/opt/databases/mydb.sq3
sqlite::memory:
sqlite:
```