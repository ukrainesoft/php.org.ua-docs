Клас PDOStatement

-   [« PDO::setAttribute](pdo.setattribute.html)
    
-   [PDOStatement::bindColumn »](pdostatement.bindcolumn.html)
    
-   [PHP Manual](index.html)
    
-   [PDO](book.pdo.html)
    
-   Клас PDOStatement
    

# Клас PDOStatement

(PHP 5> = 5.1.0, PHP 7, PHP 8, PECL pdo> = 1.0.0)

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

| Версия | Описание                                                                                                                                  |
|--------|-------------------------------------------------------------------------------------------------------------------------------------------|
|        | **PDOStatement** тепер реалізує інтерфейс [IteratorAggregate](class.iteratoraggregate.html) замість [Traversable](class.traversable.html) |

## Зміст

-   [PDOStatement::bindColumn](pdostatement.bindcolumn.html) - Зв'язує стовпець зі змінною PHP
-   [PDOStatement::bindParam](pdostatement.bindparam.html) — Прив'язує параметр запиту до змінної
-   [PDOStatement::bindValue](pdostatement.bindvalue.html) — Зв'язує параметр із заданим значенням
-   [PDOStatement::closeCursor](pdostatement.closecursor.html) — Закриває курсор, переводячи запит у стан готовності до повторного запуску
-   [PDOStatement::columnCount](pdostatement.columncount.html) — Повертає кількість стовпців у результуючому наборі
-   [PDOStatement::debugDumpParams](pdostatement.debugdumpparams.html) — Виведення інформації про підготовлену SQL-команду з метою налагодження
-   [PDOStatement::errorCode](pdostatement.errorcode.html) — Отримує код SQLSTATE, пов'язаний із останньою операцією в об'єкті PDOStatement
-   [PDOStatement::errorInfo](pdostatement.errorinfo.html) — Отримання розширеної інформації про помилку, що сталася внаслідок роботи об'єкта PDOStatement
-   [PDOStatement::execute](pdostatement.execute.html) - Запускає підготовлений запит на виконання
-   [PDOStatement::fetch](pdostatement.fetch.html) — Витяг наступного рядка з результуючого набору
-   [PDOStatement::fetchAll](pdostatement.fetchall.html) — Вибирає рядки, що залишилися, з набору результатів
-   [PDOStatement::fetchColumn](pdostatement.fetchcolumn.html) — Повертає дані одного стовпця наступного рядка результуючого набору
-   [PDOStatement::fetchObject](pdostatement.fetchobject.html) — Витягує наступний рядок і повертає його у вигляді об'єкта
-   [PDOStatement::getAttribute](pdostatement.getattribute.html) — Отримання атрибуту запиту PDOStatement
-   [PDOStatement::getColumnMeta](pdostatement.getcolumnmeta.html) — Повертає метадані стовпця у результуючій таблиці
-   [PDOStatement::getIterator](pdostatement.getiterator.html) — Отримує ітератор набору результатів
-   [PDOStatement::nextRowset](pdostatement.nextrowset.html) — Перехід до наступного набору рядків через запит
-   [PDOStatement::rowCount](pdostatement.rowcount.html) — Повертає кількість рядків, порушених останнім SQL-запитом
-   [PDOStatement::setAttribute](pdostatement.setattribute.html) — Встановлює атрибут об'єкту PDOStatement
-   [PDOStatement::setFetchMode](pdostatement.setfetchmode.html) — Встановлює режим за замовчуванням для об'єкта запиту.