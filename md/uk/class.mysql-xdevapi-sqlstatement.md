---
navigation:
  - mysql-xdevapi-session.starttransaction.md: '« Session::startTransaction'
  - mysql-xdevapi-sqlstatement.bind.md: 'SqlStatement::bind »'
  - index.md: PHP Manual
  - book.mysql-xdevapi.md: Mysqlxdevapi
title: Клас SqlStatement
---
# Клас SqlStatement

(PECL mysql-xdevapi >= 8.0.11)

## Вступ

## Огляд класів

```classsynopsis



    
     
      class mysql_xdevapi\SqlStatement
     
     {

    /* Константы */
    
     const
     int
      EXECUTE_ASYNC = 1;

    const
     int
      BUFFERED = 2;


    /* Свойства */
    public
      $statement;



    /* Методы */
    
   public bind(string $param): mysql_xdevapi\SqlStatement
public execute(): mysql_xdevapi\Result
public getNextResult(): mysql_xdevapi\Result
public getResult(): mysql_xdevapi\Result
public hasMoreResults(): bool

   }
```

## Властивості

statement

## Обумовлені константи

**`mysql_xdevapi\SqlStatement::EXECUTE_ASYNC`**

**`mysql_xdevapi\SqlStatement::BUFFERED`**

## Зміст

-   [SqlStatement::bind](mysql-xdevapi-sqlstatement.bind.md) — Зв'язує параметри затвердження
-   [SqlStatement::construct](mysql-xdevapi-sqlstatement.construct.md) - Опис конструктора
-   [SqlStatement::execute](mysql-xdevapi-sqlstatement.execute.md) — Виконує операцію
-   [SqlStatement::getNextResult](mysql-xdevapi-sqlstatement.getnextresult.md) — Отримує наступний результат
-   [SqlStatement::getResult](mysql-xdevapi-sqlstatement.getresult.md) — Отримує результат
-   [SqlStatement::hasMoreResults](mysql-xdevapi-sqlstatement.hasmoreresults.md) — Перевіряє, чи є ще результати
