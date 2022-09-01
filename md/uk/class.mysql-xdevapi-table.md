---
navigation:
  - mysql-xdevapi-statement.hasmoreresults.html: '« Statement::hasMoreResults'
  - mysql-xdevapi-table.construct.html: 'Table::construct »'
  - index.html: PHP Manual
  - book.mysql-xdevapi.html: Mysqlxdevapi
title: Клас Table
---
# Клас Table

(PECL mysql-xdevapi >= 8.0.11)

## Вступ

Надає доступ до таблиці через оператори INSERT/SELECT/UPDATE/DELETE.

## Огляд класів

```classsynopsis



    
     
      class mysql_xdevapi\Table
     

     implements 
       mysql_xdevapi\SchemaObject {

    /* Свойства */
    
     public
      $name;



    /* Методы */
    
   public count(): int
public delete(): mysql_xdevapi\TableDelete
public existsInDatabase(): bool
public getName(): string
public getSchema(): mysql_xdevapi\Schema
public getSession(): mysql_xdevapi\Session
public insert(mixed $columns, mixed ...$more_columns): mysql_xdevapi\TableInsert
public isView(): bool
public select(mixed $columns, mixed ...$more_columns): mysql_xdevapi\TableSelect
public update(): mysql_xdevapi\TableUpdate

   }
```

## Властивості

name

## Зміст

-   [Table::construct](mysql-xdevapi-table.construct.html) - Конструктор Table
-   [Table::count](mysql-xdevapi-table.count.html) — Отримати кількість рядків
-   [Table::delete](mysql-xdevapi-table.delete.html) — Видалити рядки з таблиці
-   [Table::existsInDatabase](mysql-xdevapi-table.existsindatabase.html) — Перевірити, чи існує таблиця у базі даних
-   [Table::getName](mysql-xdevapi-table.getname.html) — Отримати ім'я таблиці
-   [Table::getSchema](mysql-xdevapi-table.getschema.html) — Отримати схему таблиці
-   [Table::getSession](mysql-xdevapi-table.getsession.html) — Отримати таблицю сесій
-   [Table::insert](mysql-xdevapi-table.insert.html) — Вставити рядки таблиці
-   [Table::isView](mysql-xdevapi-table.isview.html) — Перевірити, чи таблиця є поданням
-   [Table::select](mysql-xdevapi-table.select.html) - Вибрати рядки з таблиці
-   [Table::update](mysql-xdevapi-table.update.html) — Оновити рядки у таблиці
