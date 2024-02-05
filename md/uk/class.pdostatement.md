---
navigation:
  - pdo.setattribute.md: '« PDO::setAttribute'
  - pdostatement.bindcolumn.md: 'PDOStatement::bindColumn »'
  - index.md: PHP Manual
  - book.pdo.md: PDO
title: Клас PDOStatement
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Клас PDOStatement

(PHP 5 >= 5.1.0, PHP 7, PHP 8, PECL pdo >= 1.0.0)

## Вступ

Подає підготовлений запит до бази даних, а після виконання запиту відповідний результуючий набір.

## Огляд класів

```classsynopsis

    
     class PDOStatement
    

    
     implements
      IteratorAggregate {

    /* Свойства */
    
     public
     string
      $queryString;


    /* Методы */
    
   public bindColumn(    string|int $column,    mixed &$var,    int $type = PDO::PARAM_STR,    int $maxLength = 0,    mixed $driverOptions = null): bool
public bindParam(    string|int $param,    mixed &$var,    int $type = PDO::PARAM_STR,    int $maxLength = 0,    mixed $driverOptions = null): bool
public bindValue(string|int $param, mixed $value, int $type = PDO::PARAM_STR): bool
public closeCursor(): bool
public columnCount(): int
public debugDumpParams(): ?bool
public errorCode(): ?string
public errorInfo(): array
public execute(?array $params = null): bool
public fetch(int $mode = PDO::FETCH_DEFAULT, int $cursorOrientation = PDO::FETCH_ORI_NEXT, int $cursorOffset = 0): mixed
public fetchAll(int $mode = PDO::FETCH_DEFAULT): array
public fetchAll(int $mode = PDO::FETCH_COLUMN, int $column): array
public fetchAll(int $mode = PDO::FETCH_CLASS, string $class, ?array $constructorArgs): array
public fetchAll(int $mode = PDO::FETCH_FUNC, callable $callback): array
public fetchColumn(int $column = 0): mixed
public fetchObject(?string $class = "stdClass", array $constructorArgs = []): object|false
public getAttribute(int $name): mixed
public getColumnMeta(int $column): array|false
public getIterator(): Iterator
public nextRowset(): bool
public rowCount(): int
public setAttribute(int $attribute, mixed $value): bool
public setFetchMode(int $mode): bool
public setFetchMode(int $mode = PDO::FETCH_COLUMN, int $colno): bool
public setFetchMode(int $mode = PDO::FETCH_CLASS, string $class, ?array $constructorArgs = null): bool
public setFetchMode(int $mode = PDO::FETCH_INTO, object $object): bool

   }
```

## Властивості

queryString

Використовуваний рядок запиту.

## список змін

| Версия | Опис |
| --- | --- |
| 8.0.0 | **PDOStatement** тепер реалізує інтерфейс [IteratorAggregate](class.iteratoraggregate.md) замість [Traversable](class.traversable.md) |

## Зміст

-   [PDOStatement::bindColumn](pdostatement.bindcolumn.md) \- Зв'язує стовпець зі змінною PHP
-   [PDOStatement::bindParam](pdostatement.bindparam.md)— Прив'язує параметр запиту до змінної
-   [PDOStatement::bindValue](pdostatement.bindvalue.md)— Зв'язує параметр із заданим значенням
-   [PDOStatement::closeCursor](pdostatement.closecursor.md)— Закриває курсор, переводячи запит у стан готовності до повторного запуску
-   [PDOStatement::columnCount](pdostatement.columncount.md)— Повертає кількість стовпців у результуючому наборі
-   [PDOStatement::debugDumpParams](pdostatement.debugdumpparams.md)— Виведення інформації про підготовлену SQL-команду з метою налагодження
-   [PDOStatement::errorCode](pdostatement.errorcode.md)— Отримує код SQLSTATE, пов'язаний із останньою операцією в об'єкті PDOStatement
-   [PDOStatement::errorInfo](pdostatement.errorinfo.md)— Отримання розширеної інформації про помилку, що сталася внаслідок роботи об'єкта PDOStatement
-   [PDOStatement::execute](pdostatement.execute.md) \- Запускає підготовлений запит на виконання
-   [PDOStatement::fetch](pdostatement.fetch.md)— Витяг наступного рядка з результуючого набору
-   [PDOStatement::fetchAll](pdostatement.fetchall.md)— Вибирає рядки, що залишилися, з набору результатів
-   [PDOStatement::fetchColumn](pdostatement.fetchcolumn.md)— Повертає дані одного стовпця наступного рядка результуючого набору
-   [PDOStatement::fetchObject](pdostatement.fetchobject.md)— Витягує наступний рядок і повертає його як об'єкт.
-   [PDOStatement::getAttribute](pdostatement.getattribute.md)— Отримання атрибуту запиту PDOStatement
-   [PDOStatement::getColumnMeta](pdostatement.getcolumnmeta.md)— Повертає метадані стовпця у результуючій таблиці
-   [PDOStatement::getIterator](pdostatement.getiterator.md)— Отримує ітератор набору результатів
-   [PDOStatement::nextRowset](pdostatement.nextrowset.md)— Перехід до наступного набору рядків через запит
-   [PDOStatement::rowCount](pdostatement.rowcount.md)— Повертає кількість рядків, порушених останнім SQL-запитом
-   [PDOStatement::setAttribute](pdostatement.setattribute.md)— Встановлює атрибут об'єкту PDOStatement
-   [PDOStatement::setFetchMode](pdostatement.setfetchmode.md)— Встановлює режим за замовчуванням для об'єкта запиту.
