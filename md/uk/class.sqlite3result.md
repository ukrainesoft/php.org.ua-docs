---
navigation:
  - sqlite3stmt.reset.md: '« SQLite3Stmt::reset'
  - sqlite3result.columnname.md: 'SQLite3Result::columnName »'
  - index.md: PHP Manual
  - book.sqlite3.md: SQLite3
title: Клас SQLite3Result
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Клас SQLite3Result

(PHP 5 >= 5.3.0, PHP 7, PHP 8)

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

-   [SQLite3Result::columnName](sqlite3result.columnname.md) — >Повертає ім'я n-ого стовпця
-   [SQLite3Result::columnType](sqlite3result.columntype.md) \- Повертає тип n-ного стовпця
-   [SQLite3Result::\_\_construct](sqlite3result.construct.md) \- Конструктор класу SQLite3Result
-   [SQLite3Result::fetchArray](sqlite3result.fetcharray.md)— Вибирає один рядок з результуючого набору і поміщає його в асоціативний або нумерований масив, або в обох відразу
-   [SQLite3Result::finalize](sqlite3result.finalize.md) \- Закриває результуючий набір
-   [SQLite3Result::numColumns](sqlite3result.numcolumns.md)— Повертає кількість стовпців у результуючому наборі
-   [SQLite3Result::reset](sqlite3result.reset.md)— Скидає покажчик результуючого набору на перший рядок
