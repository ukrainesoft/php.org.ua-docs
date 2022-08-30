Клас SQLite3Result

-   [« SQLite3Stmt::reset](sqlite3stmt.reset.html)
    
-   [SQLite3Result::columnName »](sqlite3result.columnname.html)
    
-   [PHP Manual](index.html)
    
-   [SQLite3](book.sqlite3.html)
    
-   Клас SQLite3Result
    

# Клас SQLite3Result

(PHP 5> = 5.3.0, PHP 7, PHP 8)

## Вступ

Клас, який надає доступ до результуючого набору SQLite 3.

## Огляд класів

```classsynopsis

     
    

    
     
      class SQLite3Result
     
     {

    /* Методы */
    
   private __construct()

    public columnName(int $column): string|false
public columnType(int $column): int|false
public fetchArray(int $mode = SQLITE3_BOTH): array|false
public finalize(): bool
public numColumns(): int
public reset(): bool

   }
```

## Зміст

-   [SQLite3Result::columnName](sqlite3result.columnname.html) — >Повертає ім'я n-ого стовпця
-   [SQLite3Result::columnType](sqlite3result.columntype.html) - Повертає тип n-ного стовпця
-   [SQLite3Result::construct](sqlite3result.construct.html) - Конструктор класу SQLite3Result
-   [SQLite3Result::fetchArray](sqlite3result.fetcharray.html) — Вибирає один рядок з результуючого набору і поміщає його в асоціативний або нумерований масив, або в обох відразу
-   [SQLite3Result::finalize](sqlite3result.finalize.html) - Закриває результуючий набір
-   [SQLite3Result::numColumns](sqlite3result.numcolumns.html) — Повертає кількість стовпців у результуючому наборі
-   [SQLite3Result::reset](sqlite3result.reset.html) — Скидає покажчик результуючого набору на перший рядок