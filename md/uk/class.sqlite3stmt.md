---
navigation:
  - class.sqlite3exception.md: « SQLite3Exception
  - sqlite3stmt.bindparam.md: 'SQLite3Stmt::bindParam »'
  - index.md: PHP Manual
  - book.sqlite3.md: SQLite3
title: Клас SQLite3Stmt
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Клас SQLite3Stmt

(PHP 5 >= 5.3.0, PHP 7, PHP 8)

## Вступ

Клас, який надає доступ до підготовлених запитів у модулі SQLite 3.

## Огляд класів

```classsynopsis

    
     class SQLite3Stmt
     {

    /* Методы */
    
   private __construct(SQLite3 $sqlite3, string $query)

    public bindParam(string|int $param, mixed &$var, int $type = SQLITE3_TEXT): bool
public bindValue(string|int $param, mixed $value, int $type = SQLITE3_TEXT): bool
public clear(): bool
public close(): bool
public execute(): SQLite3Result|false
public getSQL(bool $expand = false): string|false
public paramCount(): int
public readOnly(): bool
public reset(): bool

   }
```

## Зміст

-   [SQLite3Stmt::bindParam](sqlite3stmt.bindparam.md)— Зв'язує параметр із змінною підготовленого запиту
-   [SQLite3Stmt::bindValue](sqlite3stmt.bindvalue.md)— Зв'язує значення параметра із змінною підготовленого запиту
-   [SQLite3Stmt::clear](sqlite3stmt.clear.md)— Видаляє всі поточні параметри.
-   [SQLite3Stmt::close](sqlite3stmt.close.md) \- Закриває підготовлений запит
-   [SQLite3Stmt::\_\_construct](sqlite3stmt.construct.md) \- Конструктор класу SQLite3Stmt
-   [SQLite3Stmt::execute](sqlite3stmt.execute.md)— Виконує підготовлений запит та повертає об'єкт із результуючим набором
-   [SQLite3Stmt::getSQL](sqlite3stmt.getsql.md)— Отримати SQL-запит у вигляді рядка із запиту
-   [SQLite3Stmt::paramCount](sqlite3stmt.paramcount.md)— Повертає кількість параметрів у підготовленому запиті
-   [SQLite3Stmt::readOnly](sqlite3stmt.readonly.md)— Перевіряє, чи є підготовлений запит лише для читання
-   [SQLite3Stmt::reset](sqlite3stmt.reset.md) \- Скидає підготовлений запит
